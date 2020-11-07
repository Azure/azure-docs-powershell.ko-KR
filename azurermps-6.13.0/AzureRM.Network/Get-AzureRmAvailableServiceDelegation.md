---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
ms.openlocfilehash: bc5c09913209713df192603aff7ea7646e651699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703444"
---
# <span data-ttu-id="5f131-101">Get-AzureRmAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="5f131-101">Get-AzureRmAvailableServiceDelegation</span></span>

## <span data-ttu-id="5f131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f131-102">SYNOPSIS</span></span>
<span data-ttu-id="5f131-103">지역에서 사용 가능한 서비스 위임을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f131-103">Get available service delegations in the region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f131-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f131-104">SYNTAX</span></span>

```
Get-AzureRmAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f131-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5f131-105">DESCRIPTION</span></span>
<span data-ttu-id="5f131-106">**AzureRmAvailableServiceDelegation** cmdlet을 사용 하 여 제공 된 위치에서 서브넷에 대해 사용 가능한 모든 서비스 위임을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f131-106">The **Get-AzureRmAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="5f131-107">이 cmdlet은 단일 서브넷에 공존할 수 있는 위임을 설명 *하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f131-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="5f131-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5f131-108">EXAMPLES</span></span>

### <span data-ttu-id="5f131-109">1: 사용할 수 있는 모든 서비스 위임을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f131-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzureRmAvailableServiceDelegation -Location "westus"

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

## <span data-ttu-id="5f131-110">변수</span><span class="sxs-lookup"><span data-stu-id="5f131-110">PARAMETERS</span></span>

### <span data-ttu-id="5f131-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f131-111">-DefaultProfile</span></span>
<span data-ttu-id="5f131-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f131-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f131-113">-위치</span><span class="sxs-lookup"><span data-stu-id="5f131-113">-Location</span></span>
<span data-ttu-id="5f131-114">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5f131-114">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f131-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f131-115">CommonParameters</span></span>
<span data-ttu-id="5f131-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f131-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5f131-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f131-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f131-118">입력</span><span class="sxs-lookup"><span data-stu-id="5f131-118">INPUTS</span></span>

### <span data-ttu-id="5f131-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5f131-119">System.String</span></span>

## <span data-ttu-id="5f131-120">출력</span><span class="sxs-lookup"><span data-stu-id="5f131-120">OUTPUTS</span></span>

### <span data-ttu-id="5f131-121">Microsoft. 네트워크 모델. Ps을 통해</span><span class="sxs-lookup"><span data-stu-id="5f131-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="5f131-122">상속자</span><span class="sxs-lookup"><span data-stu-id="5f131-122">NOTES</span></span>

## <span data-ttu-id="5f131-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f131-123">RELATED LINKS</span></span>
<span data-ttu-id="5f131-124">[추가-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [새로운 AzureRmDelegation](./New-AzureRmDelegation.md) 
 [제거-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="5f131-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span></span>
