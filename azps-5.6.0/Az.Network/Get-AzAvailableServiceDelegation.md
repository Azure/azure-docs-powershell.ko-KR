---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: d98b9d2395c0795c37fd9d7cf31dc354bde3b7cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993846"
---
# <span data-ttu-id="503ca-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="503ca-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="503ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="503ca-102">SYNOPSIS</span></span>
<span data-ttu-id="503ca-103">지역에서 사용 가능한 서비스 위임을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="503ca-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="503ca-104">구문</span><span class="sxs-lookup"><span data-stu-id="503ca-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="503ca-105">설명</span><span class="sxs-lookup"><span data-stu-id="503ca-105">DESCRIPTION</span></span>
<span data-ttu-id="503ca-106">**Get-AzAvailableServiceDelegation** cmdlet을 사용하면 제공된 위치에서 서브넷에 대해 사용 가능한 모든 서비스 위임을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="503ca-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="503ca-107">이 cmdlet은  단일 서브넷에 공존할 수 있는 위임에 대해 설명하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="503ca-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="503ca-108">예제</span><span class="sxs-lookup"><span data-stu-id="503ca-108">EXAMPLES</span></span>

### <span data-ttu-id="503ca-109">1: 사용 가능한 모든 서비스 위임 사용</span><span class="sxs-lookup"><span data-stu-id="503ca-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzAvailableServiceDelegation -Location "westus"

Name        : Microsoft.Web.serverFarms
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Web.serverFarms
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Web/serverFarms
Actions     : {Microsoft.Network/virtualNetworks/subnets/action}

Name        : Microsoft.Sql.servers
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Sql.servers
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Sql/servers
Actions     : {}
```

## <span data-ttu-id="503ca-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="503ca-110">PARAMETERS</span></span>

### <span data-ttu-id="503ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="503ca-111">-DefaultProfile</span></span>
<span data-ttu-id="503ca-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="503ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="503ca-113">-Location</span><span class="sxs-lookup"><span data-stu-id="503ca-113">-Location</span></span>
<span data-ttu-id="503ca-114">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="503ca-114">The location.</span></span>

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

### <span data-ttu-id="503ca-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="503ca-115">CommonParameters</span></span>
<span data-ttu-id="503ca-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="503ca-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="503ca-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="503ca-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="503ca-118">입력</span><span class="sxs-lookup"><span data-stu-id="503ca-118">INPUTS</span></span>

### <span data-ttu-id="503ca-119">System.String</span><span class="sxs-lookup"><span data-stu-id="503ca-119">System.String</span></span>

## <span data-ttu-id="503ca-120">출력</span><span class="sxs-lookup"><span data-stu-id="503ca-120">OUTPUTS</span></span>

### <span data-ttu-id="503ca-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="503ca-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="503ca-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="503ca-122">NOTES</span></span>

## <span data-ttu-id="503ca-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="503ca-123">RELATED LINKS</span></span>

<span data-ttu-id="503ca-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="503ca-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>