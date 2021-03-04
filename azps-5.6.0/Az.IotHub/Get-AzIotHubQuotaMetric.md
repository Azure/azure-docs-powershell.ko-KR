---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 70e63723bd9647f003082813cd680a84ae5638c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987919"
---
# <span data-ttu-id="ae898-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="ae898-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="ae898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae898-102">SYNOPSIS</span></span>
<span data-ttu-id="ae898-103">IotHub에 대한 할당량 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ae898-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="ae898-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae898-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae898-105">설명</span><span class="sxs-lookup"><span data-stu-id="ae898-105">DESCRIPTION</span></span>
<span data-ttu-id="ae898-106">IotHub에 대한 할당량 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ae898-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="ae898-107">예제</span><span class="sxs-lookup"><span data-stu-id="ae898-107">EXAMPLES</span></span>

### <span data-ttu-id="ae898-108">예제 1 할당량 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ae898-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ae898-109">"myiothub"라는 IotHub에 대한 할당량 메트릭 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ae898-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ae898-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ae898-110">PARAMETERS</span></span>

### <span data-ttu-id="ae898-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae898-111">-DefaultProfile</span></span>
<span data-ttu-id="ae898-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ae898-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae898-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ae898-113">-Name</span></span>
<span data-ttu-id="ae898-114">IoT 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae898-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae898-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae898-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae898-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ae898-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae898-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae898-117">CommonParameters</span></span>
<span data-ttu-id="ae898-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae898-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae898-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ae898-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae898-120">입력</span><span class="sxs-lookup"><span data-stu-id="ae898-120">INPUTS</span></span>

### <span data-ttu-id="ae898-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ae898-121">System.String</span></span>

## <span data-ttu-id="ae898-122">출력</span><span class="sxs-lookup"><span data-stu-id="ae898-122">OUTPUTS</span></span>

### <span data-ttu-id="ae898-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="ae898-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="ae898-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae898-124">NOTES</span></span>

## <span data-ttu-id="ae898-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae898-125">RELATED LINKS</span></span>
