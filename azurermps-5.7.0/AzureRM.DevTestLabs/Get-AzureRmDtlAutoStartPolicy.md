---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: c61739c3bd80c5c5c15c7e10d8a787f45c44ec69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702533"
---
# <span data-ttu-id="f8850-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="f8850-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="f8850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8850-102">SYNOPSIS</span></span>
<span data-ttu-id="f8850-103">DevTest Labs의 랩에 대 한 자동 시작 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8850-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8850-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8850-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8850-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f8850-105">DESCRIPTION</span></span>
<span data-ttu-id="f8850-106">**AzureRmDtlAutoStartPolicy** cmdlet은 자동 시작을 위해 랩 가상 컴퓨터를 예약 하는 랩의 자동 시작 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8850-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="f8850-107">Cmdlet은 정책의 사용 또는 사용 안 함 상태와 자동 시작에 대 한 랩 가상 컴퓨터의 예약을 허용 하도록 설정한 요일 및 시간을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8850-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="f8850-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f8850-108">EXAMPLES</span></span>

## <span data-ttu-id="f8850-109">변수</span><span class="sxs-lookup"><span data-stu-id="f8850-109">PARAMETERS</span></span>

### <span data-ttu-id="f8850-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8850-110">-DefaultProfile</span></span>
<span data-ttu-id="f8850-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f8850-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8850-112">-시 이름</span><span class="sxs-lookup"><span data-stu-id="f8850-112">-LabName</span></span>
<span data-ttu-id="f8850-113">이 cmdlet이 자동 시작 정책을 가져오는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8850-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8850-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8850-114">-ResourceGroupName</span></span>
<span data-ttu-id="f8850-115">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8850-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8850-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8850-116">CommonParameters</span></span>
<span data-ttu-id="f8850-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8850-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8850-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8850-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8850-119">입력</span><span class="sxs-lookup"><span data-stu-id="f8850-119">INPUTS</span></span>

### <span data-ttu-id="f8850-120">않아야</span><span class="sxs-lookup"><span data-stu-id="f8850-120">None</span></span>
<span data-ttu-id="f8850-121">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8850-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8850-122">출력</span><span class="sxs-lookup"><span data-stu-id="f8850-122">OUTPUTS</span></span>

### <span data-ttu-id="f8850-123">Microsoft. DevTestLabs. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="f8850-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="f8850-124">이 cmdlet은 랩의 가상 컴퓨터를 시작 해야 하는 시점을 지정 하는 일정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8850-124">This cmdlet returns the schedule that specifies when the lab's virtual machines must be started.</span></span>

## <span data-ttu-id="f8850-125">상속자</span><span class="sxs-lookup"><span data-stu-id="f8850-125">NOTES</span></span>

## <span data-ttu-id="f8850-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8850-126">RELATED LINKS</span></span>

[<span data-ttu-id="f8850-127">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="f8850-127">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


