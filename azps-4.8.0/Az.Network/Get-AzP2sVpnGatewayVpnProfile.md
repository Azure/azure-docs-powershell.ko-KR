---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204020"
---
# <span data-ttu-id="28a1d-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="28a1d-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="28a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="28a1d-103">사이트 클라이언트 설정에 대 한 Vpn 프로필을 다운로드 하 여 P2SVpnGateway에 사이트 연결을 지정 하는 경우 고객이 사용할 수 있는 SAS url을 생성 하 고 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28a1d-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="28a1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28a1d-104">SYNTAX</span></span>

### <span data-ttu-id="28a1d-105">ByP2SVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="28a1d-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28a1d-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="28a1d-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28a1d-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="28a1d-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28a1d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="28a1d-108">DESCRIPTION</span></span>
<span data-ttu-id="28a1d-109">**AzP2sVpnGatewayVpnProfile** cmdlet을 사용 하면 사이트 클라이언트 설정에 대 한 Vpn 프로필을 다운로드 하 여 P2SVpnGateway에 사이트를 연결 하는 데 사용할 수 있는 sa url을 생성 하 고 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28a1d-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="28a1d-110">이 Vpn 프로필을 사용 하는 사이트 클라이언트 설정에 대 한 가리키기는이 특정 P2SVpnGateway에만 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28a1d-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="28a1d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="28a1d-111">EXAMPLES</span></span>

### <span data-ttu-id="28a1d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="28a1d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="28a1d-113">**AzP2sVpnGatewayVpnProfile** cmdlet을 사용 하면 사이트 클라이언트 설정에 대 한 Vpn 프로필을 다운로드 하 여 P2SVpnGateway에 사이트를 연결 하는 데 사용할 수 있는 sa url을 생성 하 고 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28a1d-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="28a1d-114">ProfileUrl은 고객이 사이트 클라이언트 설치 지점에 대 한 Vpn 프로필을 다운로드할 수 있는 SAS url을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28a1d-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="28a1d-115">변수</span><span class="sxs-lookup"><span data-stu-id="28a1d-115">PARAMETERS</span></span>

### <span data-ttu-id="28a1d-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="28a1d-116">-AuthenticationMethod</span></span>
<span data-ttu-id="28a1d-117">인증 방법</span><span class="sxs-lookup"><span data-stu-id="28a1d-117">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a1d-118">-DefaultProfile</span></span>
<span data-ttu-id="28a1d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28a1d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a1d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28a1d-120">-InputObject</span></span>
<span data-ttu-id="28a1d-121">수정할 p2s vpn 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="28a1d-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28a1d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="28a1d-122">-Name</span></span>
<span data-ttu-id="28a1d-123">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28a1d-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a1d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a1d-124">-ResourceGroupName</span></span>
<span data-ttu-id="28a1d-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28a1d-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a1d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28a1d-126">-ResourceId</span></span>
<span data-ttu-id="28a1d-127">수정할 P2SVpnGateway의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="28a1d-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28a1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a1d-128">CommonParameters</span></span>
<span data-ttu-id="28a1d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28a1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a1d-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28a1d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a1d-131">입력</span><span class="sxs-lookup"><span data-stu-id="28a1d-131">INPUTS</span></span>

### <span data-ttu-id="28a1d-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28a1d-132">System.String</span></span>
<span data-ttu-id="28a1d-133">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="28a1d-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="28a1d-134">출력</span><span class="sxs-lookup"><span data-stu-id="28a1d-134">OUTPUTS</span></span>

### <span data-ttu-id="28a1d-135">PSVpnProfileResponse에 대 한.</span><span class="sxs-lookup"><span data-stu-id="28a1d-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="28a1d-136">상속자</span><span class="sxs-lookup"><span data-stu-id="28a1d-136">NOTES</span></span>

## <span data-ttu-id="28a1d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28a1d-137">RELATED LINKS</span></span>
