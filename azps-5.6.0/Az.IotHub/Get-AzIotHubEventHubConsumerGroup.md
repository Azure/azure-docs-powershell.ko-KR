---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: f4a722ad01cf354cc49b3441c03ec8aaca2e5e57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988003"
---
# <span data-ttu-id="fabcd-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fabcd-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="fabcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fabcd-102">SYNOPSIS</span></span>
<span data-ttu-id="fabcd-103">모든 eventhub 소비자group을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fabcd-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="fabcd-104">구문</span><span class="sxs-lookup"><span data-stu-id="fabcd-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fabcd-105">설명</span><span class="sxs-lookup"><span data-stu-id="fabcd-105">DESCRIPTION</span></span>
<span data-ttu-id="fabcd-106">IotHub에서 사용하는 다양한 EventHubs에 대한 모든 eventhub 소비자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fabcd-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="fabcd-107">예제</span><span class="sxs-lookup"><span data-stu-id="fabcd-107">EXAMPLES</span></span>

### <span data-ttu-id="fabcd-108">예제 1 원격 분석 eventhub에 대한 모든 eventhub 소비자group을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fabcd-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="fabcd-109">myiothub라는 iothub에 대한 원격 분석 eventhub에 대한 모든 eventhub 소비자group을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fabcd-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="fabcd-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fabcd-110">PARAMETERS</span></span>

### <span data-ttu-id="fabcd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabcd-111">-DefaultProfile</span></span>
<span data-ttu-id="fabcd-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fabcd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fabcd-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fabcd-113">-Name</span></span>
<span data-ttu-id="fabcd-114">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="fabcd-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="fabcd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fabcd-115">-ResourceGroupName</span></span>
<span data-ttu-id="fabcd-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fabcd-116">Resource Group Name</span></span>

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

### <span data-ttu-id="fabcd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabcd-117">CommonParameters</span></span>
<span data-ttu-id="fabcd-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fabcd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabcd-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fabcd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabcd-120">입력</span><span class="sxs-lookup"><span data-stu-id="fabcd-120">INPUTS</span></span>

### <span data-ttu-id="fabcd-121">System.String</span><span class="sxs-lookup"><span data-stu-id="fabcd-121">System.String</span></span>

## <span data-ttu-id="fabcd-122">출력</span><span class="sxs-lookup"><span data-stu-id="fabcd-122">OUTPUTS</span></span>

### <span data-ttu-id="fabcd-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="fabcd-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="fabcd-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fabcd-124">NOTES</span></span>

## <span data-ttu-id="fabcd-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fabcd-125">RELATED LINKS</span></span>
