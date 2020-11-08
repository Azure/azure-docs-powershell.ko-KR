---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226571"
---
# <span data-ttu-id="5de79-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="5de79-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="5de79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5de79-102">SYNOPSIS</span></span>
<span data-ttu-id="5de79-103">사이트 클라이언트 설치 지점에 대 한 VirtualWan-VpnServerConfiguration 수준에서 Vpn 프로필을 생성 하 고 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="5de79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5de79-104">SYNTAX</span></span>

### <span data-ttu-id="5de79-105">ByVirtualWanNameByVpnServerConfigurationObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="5de79-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5de79-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="5de79-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5de79-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="5de79-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5de79-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="5de79-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5de79-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="5de79-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5de79-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="5de79-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5de79-111">설명은</span><span class="sxs-lookup"><span data-stu-id="5de79-111">DESCRIPTION</span></span>
<span data-ttu-id="5de79-112">**AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet을 사용 하면 사이트 클라이언트 설치 지점에 대 한 VirtualWan-VpnServerConfiguration 수준에서 Vpn 프로필을 생성 하 고 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="5de79-113">이는 사이트에서 사이트 클라이언트를 Azure P2SVpnGateway로 연결 하는 데 필요한 시점입니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="5de79-114">예제의</span><span class="sxs-lookup"><span data-stu-id="5de79-114">EXAMPLES</span></span>

### <span data-ttu-id="5de79-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="5de79-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="5de79-116">위 명령에서는 고객이 사이트 클라이언트 설치 지점에 대 한 VirtualWan-VpnServerConfiguration 수준에서 Vpn 프로필을 다운로드 하는 데 사용할 수 있는 SAS Url을 생성 하 고 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="5de79-117">변수</span><span class="sxs-lookup"><span data-stu-id="5de79-117">PARAMETERS</span></span>

### <span data-ttu-id="5de79-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="5de79-118">-AuthenticationMethod</span></span>
<span data-ttu-id="5de79-119">인증 방법</span><span class="sxs-lookup"><span data-stu-id="5de79-119">Authentication Method</span></span>

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

### <span data-ttu-id="5de79-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de79-120">-DefaultProfile</span></span>
<span data-ttu-id="5de79-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5de79-122">-이름</span><span class="sxs-lookup"><span data-stu-id="5de79-122">-Name</span></span>
<span data-ttu-id="5de79-123">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de79-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5de79-124">-ResourceGroupName</span></span>
<span data-ttu-id="5de79-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de79-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5de79-126">-ResourceId</span></span>
<span data-ttu-id="5de79-127">가상 wan에 대 한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5de79-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="5de79-128">-VirtualWanObject</span></span>
<span data-ttu-id="5de79-129">가상 wan 개체.</span><span class="sxs-lookup"><span data-stu-id="5de79-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5de79-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="5de79-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="5de79-131">이 VirtualWan이 연결 된 VpnServerConfiguration입니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5de79-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5de79-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="5de79-133">이 가상 wan이 연결 되는 Vpn 서버 configuraiton 개체의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5de79-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de79-134">CommonParameters</span></span>
<span data-ttu-id="5de79-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5de79-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de79-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5de79-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de79-137">입력</span><span class="sxs-lookup"><span data-stu-id="5de79-137">INPUTS</span></span>

### <span data-ttu-id="5de79-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5de79-138">System.String</span></span>
<span data-ttu-id="5de79-139">PSVpnServerConfiguration. a \* PSVirtualWan Microsoft Azure. 네트워크. 모델.</span><span class="sxs-lookup"><span data-stu-id="5de79-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="5de79-140">출력</span><span class="sxs-lookup"><span data-stu-id="5de79-140">OUTPUTS</span></span>

### <span data-ttu-id="5de79-141">PSVpnProfileResponse에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5de79-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="5de79-142">상속자</span><span class="sxs-lookup"><span data-stu-id="5de79-142">NOTES</span></span>

## <span data-ttu-id="5de79-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5de79-143">RELATED LINKS</span></span>
