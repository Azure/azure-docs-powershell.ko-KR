---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9934ea8ba32fc1d63353e83303cfe8371629bca1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875883"
---
# <span data-ttu-id="161c3-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="161c3-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="161c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="161c3-102">SYNOPSIS</span></span>
<span data-ttu-id="161c3-103">모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="161c3-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="161c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="161c3-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="161c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="161c3-105">DESCRIPTION</span></span>
<span data-ttu-id="161c3-106">IotHub에서 사용 하는 다른 EventHubs에 대 한 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="161c3-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="161c3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="161c3-107">EXAMPLES</span></span>

### <span data-ttu-id="161c3-108">예제 1 원격 분석 eventhub에 대 한 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="161c3-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="161c3-109">Myiothub iothub에 대 한 원격 분석 eventhub의 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="161c3-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="161c3-110">변수</span><span class="sxs-lookup"><span data-stu-id="161c3-110">PARAMETERS</span></span>

### <span data-ttu-id="161c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="161c3-111">-DefaultProfile</span></span>
<span data-ttu-id="161c3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="161c3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="161c3-113">-이름</span><span class="sxs-lookup"><span data-stu-id="161c3-113">-Name</span></span>
<span data-ttu-id="161c3-114">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="161c3-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="161c3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="161c3-115">-ResourceGroupName</span></span>
<span data-ttu-id="161c3-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="161c3-116">Resource Group Name</span></span>

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

### <span data-ttu-id="161c3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="161c3-117">CommonParameters</span></span>
<span data-ttu-id="161c3-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="161c3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="161c3-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="161c3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="161c3-120">입력</span><span class="sxs-lookup"><span data-stu-id="161c3-120">INPUTS</span></span>

### <span data-ttu-id="161c3-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="161c3-121">System.String</span></span>

## <span data-ttu-id="161c3-122">출력</span><span class="sxs-lookup"><span data-stu-id="161c3-122">OUTPUTS</span></span>

### <span data-ttu-id="161c3-123">IotHub. PSEventHubConsumerGroupInfo/. \*</span><span class="sxs-lookup"><span data-stu-id="161c3-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="161c3-124">상속자</span><span class="sxs-lookup"><span data-stu-id="161c3-124">NOTES</span></span>

## <span data-ttu-id="161c3-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="161c3-125">RELATED LINKS</span></span>
