package Core;

import Entities.Campaign;
import Entities.Game;
import Entities.Gamer;
import concirete.CampaignManager;
import concirete.GameManager;
import concirete.GamerManager;
import concirete.SalesManeger;

public class Main {

	public static void main(String[] args) {
		
		Gamer gamer = new Gamer(216,"mehmet ali","yalçın","1998");
		Gamer gamer2 = new Gamer(217,"mert","yalçın","2013");
		GamerManager gamerManager = new GamerManager();
		gamerManager.addGamer(gamer);
		
		Game game = new Game("pubg",150);
		GameManager gameManager = new GameManager();
		gameManager.addGame(game);
		
		SalesManeger salesManager  = new SalesManeger();
		salesManager.buy(game, gamer);
		
		Campaign campaign = new Campaign(18, "yaz indirimleri");
		CampaignManager campaignManager = new CampaignManager();
		campaignManager.addCampaign(campaign);
		
		campaignManager.addToGame(campaign, game);
		gameManager.updateGame(game);
		
		salesManager.buy(game,gamer2);
		
		
