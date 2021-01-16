---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361117"
---
# <span data-ttu-id="d1c3e-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d1c3e-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="d1c3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c3e-103">모든 eventhub 소비자group을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="d1c3e-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1c3e-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1c3e-105">설명</span><span class="sxs-lookup"><span data-stu-id="d1c3e-105">DESCRIPTION</span></span>
<span data-ttu-id="d1c3e-106">IotHub에서 사용하는 다른 EventHubs에 대한 모든 eventhub 소비자group을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="d1c3e-107">예제</span><span class="sxs-lookup"><span data-stu-id="d1c3e-107">EXAMPLES</span></span>

### <span data-ttu-id="d1c3e-108">예제 1은 원격 분석 eventhub에 대한 모든 eventhub 소비자group을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d1c3e-109">myiothub라는 iothub에 대한 원격 분석 eventhub에 대한 모든 eventhub 소비자group을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="d1c3e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1c3e-110">PARAMETERS</span></span>

### <span data-ttu-id="d1c3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c3e-111">-DefaultProfile</span></span>
<span data-ttu-id="d1c3e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d1c3e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1c3e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d1c3e-113">-Name</span></span>
<span data-ttu-id="d1c3e-114">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="d1c3e-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="d1c3e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c3e-115">-ResourceGroupName</span></span>
<span data-ttu-id="d1c3e-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d1c3e-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d1c3e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c3e-117">CommonParameters</span></span>
<span data-ttu-id="d1c3e-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c3e-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1c3e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c3e-120">입력</span><span class="sxs-lookup"><span data-stu-id="d1c3e-120">INPUTS</span></span>

### <span data-ttu-id="d1c3e-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d1c3e-121">System.String</span></span>

## <span data-ttu-id="d1c3e-122">출력</span><span class="sxs-lookup"><span data-stu-id="d1c3e-122">OUTPUTS</span></span>

### <span data-ttu-id="d1c3e-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="d1c3e-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="d1c3e-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1c3e-124">NOTES</span></span>

## <span data-ttu-id="d1c3e-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1c3e-125">RELATED LINKS</span></span>
