---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338097"
---
# <span data-ttu-id="dc19b-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="dc19b-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="dc19b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc19b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc19b-103">지역에서 사용 가능한 서비스 위임을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc19b-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="dc19b-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc19b-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc19b-105">설명</span><span class="sxs-lookup"><span data-stu-id="dc19b-105">DESCRIPTION</span></span>
<span data-ttu-id="dc19b-106">**Get-AzAvailableServiceDelegation** cmdlet을 사용하면 제공된 위치에서 서브넷에 사용 가능한 모든 서비스 위임을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc19b-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="dc19b-107">이 cmdlet은 *단일* 서브넷에 공존할 수 있는 위임에 대해 설명하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc19b-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="dc19b-108">예제</span><span class="sxs-lookup"><span data-stu-id="dc19b-108">EXAMPLES</span></span>

### <span data-ttu-id="dc19b-109">1: 사용 가능한 모든 서비스 위임 사용</span><span class="sxs-lookup"><span data-stu-id="dc19b-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="dc19b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc19b-110">PARAMETERS</span></span>

### <span data-ttu-id="dc19b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc19b-111">-DefaultProfile</span></span>
<span data-ttu-id="dc19b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc19b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc19b-113">-Location</span><span class="sxs-lookup"><span data-stu-id="dc19b-113">-Location</span></span>
<span data-ttu-id="dc19b-114">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dc19b-114">The location.</span></span>

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

### <span data-ttu-id="dc19b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc19b-115">CommonParameters</span></span>
<span data-ttu-id="dc19b-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc19b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc19b-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dc19b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc19b-118">입력</span><span class="sxs-lookup"><span data-stu-id="dc19b-118">INPUTS</span></span>

### <span data-ttu-id="dc19b-119">System.String</span><span class="sxs-lookup"><span data-stu-id="dc19b-119">System.String</span></span>

## <span data-ttu-id="dc19b-120">출력</span><span class="sxs-lookup"><span data-stu-id="dc19b-120">OUTPUTS</span></span>

### <span data-ttu-id="dc19b-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="dc19b-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="dc19b-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc19b-122">NOTES</span></span>

## <span data-ttu-id="dc19b-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc19b-123">RELATED LINKS</span></span>

<span data-ttu-id="dc19b-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="dc19b-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>