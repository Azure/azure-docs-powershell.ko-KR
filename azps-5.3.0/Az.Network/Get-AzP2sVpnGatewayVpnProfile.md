---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496687"
---
# <span data-ttu-id="40dee-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="40dee-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="40dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40dee-102">SYNOPSIS</span></span>
<span data-ttu-id="40dee-103">고객이 P2SVpnGateway에 지점 및 사이트 연결을 설정하기 위해 지점 및 사이트 클라이언트 설정에 대한 VPN 프로필을 다운로드할 수 있도록 SAS URL을 생성하고 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="40dee-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="40dee-104">구문</span><span class="sxs-lookup"><span data-stu-id="40dee-104">SYNTAX</span></span>

### <span data-ttu-id="40dee-105">ByP2SVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="40dee-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40dee-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="40dee-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40dee-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="40dee-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40dee-108">설명</span><span class="sxs-lookup"><span data-stu-id="40dee-108">DESCRIPTION</span></span>
<span data-ttu-id="40dee-109">**Get-AzP2sVpnGatewayVpnProfile** cmdlet을 사용하면 고객이 P2SVpnGateway에 지점 및 사이트 연결을 설정하기 위한 지점 및 사이트 클라이언트 설정에 대한 VPN 프로필을 다운로드하기 위한 SAS URL을 생성하고 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40dee-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="40dee-110">이 Vpn 프로필을 사용하여 지점 및 사이트 대 사이트 클라이언트 설정은 이 특정 P2SVpnGateway에만 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40dee-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="40dee-111">예제</span><span class="sxs-lookup"><span data-stu-id="40dee-111">EXAMPLES</span></span>

### <span data-ttu-id="40dee-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="40dee-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="40dee-113">**Get-AzP2sVpnGatewayVpnProfile** cmdlet을 사용하면 고객이 P2SVpnGateway에 지점 및 사이트 연결을 설정하기 위한 지점 및 사이트 클라이언트 설정에 대한 VPN 프로필을 다운로드하기 위한 SAS URL을 생성하고 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40dee-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="40dee-114">ProfileUrl은 고객이 지점 및 사이트 클라이언트 설정에 대한 Vpn 프로필을 다운로드할 수 있는 SAS URL을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="40dee-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="40dee-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40dee-115">PARAMETERS</span></span>

### <span data-ttu-id="40dee-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="40dee-116">-AuthenticationMethod</span></span>
<span data-ttu-id="40dee-117">인증 방법</span><span class="sxs-lookup"><span data-stu-id="40dee-117">Authentication Method</span></span>

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

### <span data-ttu-id="40dee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40dee-118">-DefaultProfile</span></span>
<span data-ttu-id="40dee-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40dee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40dee-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40dee-120">-InputObject</span></span>
<span data-ttu-id="40dee-121">수정할 p2s vpn Gateway 개체</span><span class="sxs-lookup"><span data-stu-id="40dee-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="40dee-122">-Name</span><span class="sxs-lookup"><span data-stu-id="40dee-122">-Name</span></span>
<span data-ttu-id="40dee-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40dee-123">The resource name.</span></span>

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

### <span data-ttu-id="40dee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40dee-124">-ResourceGroupName</span></span>
<span data-ttu-id="40dee-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40dee-125">The resource group name.</span></span>

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

### <span data-ttu-id="40dee-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40dee-126">-ResourceId</span></span>
<span data-ttu-id="40dee-127">수정할 P2SVpnGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="40dee-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="40dee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40dee-128">CommonParameters</span></span>
<span data-ttu-id="40dee-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40dee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40dee-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="40dee-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40dee-131">입력</span><span class="sxs-lookup"><span data-stu-id="40dee-131">INPUTS</span></span>

### <span data-ttu-id="40dee-132">System.String</span><span class="sxs-lookup"><span data-stu-id="40dee-132">System.String</span></span>
<span data-ttu-id="40dee-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="40dee-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="40dee-134">출력</span><span class="sxs-lookup"><span data-stu-id="40dee-134">OUTPUTS</span></span>

### <span data-ttu-id="40dee-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="40dee-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="40dee-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40dee-136">NOTES</span></span>

## <span data-ttu-id="40dee-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40dee-137">RELATED LINKS</span></span>
