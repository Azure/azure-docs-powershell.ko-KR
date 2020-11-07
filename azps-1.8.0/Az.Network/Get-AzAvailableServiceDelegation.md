---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 547069954ada24531e1551b75c4065416eeae1fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700620"
---
# <span data-ttu-id="302f4-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="302f4-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="302f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="302f4-102">SYNOPSIS</span></span>
<span data-ttu-id="302f4-103">지역에서 사용 가능한 서비스 위임을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="302f4-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="302f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="302f4-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="302f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="302f4-105">DESCRIPTION</span></span>
<span data-ttu-id="302f4-106">**AzAvailableServiceDelegation** cmdlet을 사용 하 여 제공 된 위치에서 서브넷에 대해 사용 가능한 모든 서비스 위임을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="302f4-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="302f4-107">이 cmdlet은 단일 서브넷에 공존할 수 있는 위임을 설명 *하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="302f4-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="302f4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="302f4-108">EXAMPLES</span></span>

### <span data-ttu-id="302f4-109">1: 사용할 수 있는 모든 서비스 위임을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="302f4-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="302f4-110">변수</span><span class="sxs-lookup"><span data-stu-id="302f4-110">PARAMETERS</span></span>

### <span data-ttu-id="302f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302f4-111">-DefaultProfile</span></span>
<span data-ttu-id="302f4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="302f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="302f4-113">-위치</span><span class="sxs-lookup"><span data-stu-id="302f4-113">-Location</span></span>
<span data-ttu-id="302f4-114">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="302f4-114">The location.</span></span>

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

### <span data-ttu-id="302f4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302f4-115">CommonParameters</span></span>
<span data-ttu-id="302f4-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="302f4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302f4-117">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="302f4-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302f4-118">입력</span><span class="sxs-lookup"><span data-stu-id="302f4-118">INPUTS</span></span>

### <span data-ttu-id="302f4-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="302f4-119">System.String</span></span>

## <span data-ttu-id="302f4-120">출력</span><span class="sxs-lookup"><span data-stu-id="302f4-120">OUTPUTS</span></span>

### <span data-ttu-id="302f4-121">Microsoft. 네트워크 모델. Ps을 통해</span><span class="sxs-lookup"><span data-stu-id="302f4-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="302f4-122">상속자</span><span class="sxs-lookup"><span data-stu-id="302f4-122">NOTES</span></span>

## <span data-ttu-id="302f4-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="302f4-123">RELATED LINKS</span></span>

<span data-ttu-id="302f4-124">[추가-AzDelegation](./Add-AzDelegation.md) 
 [새로운 AzDelegation](./New-AzDelegation.md) 
 [제거-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="302f4-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>