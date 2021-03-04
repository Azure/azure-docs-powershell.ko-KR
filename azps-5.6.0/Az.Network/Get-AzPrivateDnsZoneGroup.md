---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: f9428c2249cf69d366a6770d448e82618d98896f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954235"
---
# <span data-ttu-id="a6f35-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="a6f35-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a6f35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6f35-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f35-103">개인 DNS 영역 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f35-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="a6f35-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6f35-104">SYNTAX</span></span>

### <span data-ttu-id="a6f35-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="a6f35-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6f35-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="a6f35-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6f35-107">설명</span><span class="sxs-lookup"><span data-stu-id="a6f35-107">DESCRIPTION</span></span>
<span data-ttu-id="a6f35-108">**Get-AzPrivateDnsZoneGroup** cmdlet은 하나 이상의 개인 DNS 영역 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f35-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="a6f35-109">예제</span><span class="sxs-lookup"><span data-stu-id="a6f35-109">EXAMPLES</span></span>

### <span data-ttu-id="a6f35-110">예제 1: 개인 DNS 영역 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="a6f35-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="a6f35-111">위의 예제에서는 리소스 그룹 rg에서 dnsgroup1이라는 개인 DNS 영역 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f35-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="a6f35-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a6f35-112">PARAMETERS</span></span>

### <span data-ttu-id="a6f35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f35-113">-DefaultProfile</span></span>
<span data-ttu-id="a6f35-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f35-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f35-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a6f35-115">-Name</span></span>
<span data-ttu-id="a6f35-116">개인 dns 영역 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f35-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6f35-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="a6f35-117">-PrivateEndpointName</span></span>
<span data-ttu-id="a6f35-118">개인 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f35-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6f35-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6f35-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6f35-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f35-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6f35-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f35-121">CommonParameters</span></span>
<span data-ttu-id="a6f35-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f35-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f35-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6f35-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f35-124">입력</span><span class="sxs-lookup"><span data-stu-id="a6f35-124">INPUTS</span></span>

### <span data-ttu-id="a6f35-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a6f35-125">System.String</span></span>

## <span data-ttu-id="a6f35-126">출력</span><span class="sxs-lookup"><span data-stu-id="a6f35-126">OUTPUTS</span></span>

### <span data-ttu-id="a6f35-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="a6f35-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="a6f35-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6f35-128">NOTES</span></span>

## <span data-ttu-id="a6f35-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6f35-129">RELATED LINKS</span></span>
