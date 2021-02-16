---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185665"
---
# <span data-ttu-id="9b805-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="9b805-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="9b805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b805-102">SYNOPSIS</span></span>
<span data-ttu-id="9b805-103">IotHub에 대한 할당량 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b805-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="9b805-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b805-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b805-105">설명</span><span class="sxs-lookup"><span data-stu-id="9b805-105">DESCRIPTION</span></span>
<span data-ttu-id="9b805-106">IotHub에 대한 할당량 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b805-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="9b805-107">예제</span><span class="sxs-lookup"><span data-stu-id="9b805-107">EXAMPLES</span></span>

### <span data-ttu-id="9b805-108">예제 1 할당량 메트릭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b805-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9b805-109">"myiothub"라는 IotHub에 대한 할당량 메트릭 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b805-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9b805-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b805-110">PARAMETERS</span></span>

### <span data-ttu-id="9b805-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b805-111">-DefaultProfile</span></span>
<span data-ttu-id="9b805-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9b805-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b805-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9b805-113">-Name</span></span>
<span data-ttu-id="9b805-114">IoT Hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b805-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="9b805-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b805-115">-ResourceGroupName</span></span>
<span data-ttu-id="9b805-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9b805-116">Resource Group Name</span></span>

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

### <span data-ttu-id="9b805-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b805-117">CommonParameters</span></span>
<span data-ttu-id="9b805-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b805-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b805-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9b805-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b805-120">입력</span><span class="sxs-lookup"><span data-stu-id="9b805-120">INPUTS</span></span>

### <span data-ttu-id="9b805-121">System.String</span><span class="sxs-lookup"><span data-stu-id="9b805-121">System.String</span></span>

## <span data-ttu-id="9b805-122">출력</span><span class="sxs-lookup"><span data-stu-id="9b805-122">OUTPUTS</span></span>

### <span data-ttu-id="9b805-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="9b805-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="9b805-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b805-124">NOTES</span></span>

## <span data-ttu-id="9b805-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b805-125">RELATED LINKS</span></span>
