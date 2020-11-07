---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 000c9f2748bd1f80559d9fc80c206e4f1c9bf0c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703284"
---
# <span data-ttu-id="2acf3-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="2acf3-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="2acf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2acf3-102">SYNOPSIS</span></span>
<span data-ttu-id="2acf3-103">DevTest 랩에서 랩에서 자동 시작 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2acf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2acf3-104">SYNTAX</span></span>

### <span data-ttu-id="2acf3-105">사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2acf3-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2acf3-106">설정할</span><span class="sxs-lookup"><span data-stu-id="2acf3-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2acf3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2acf3-107">DESCRIPTION</span></span>
<span data-ttu-id="2acf3-108">**AzureRmDtlAutoStartPolicy** cmdlet은 랩의 자동 시작 정책을 설정 하 여 랩 가상 컴퓨터에 자동 시작을 예약할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="2acf3-109">Cmdlet은 지정 된 리소스 그룹 및 랩의 이름을 사용 하 여 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="2acf3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2acf3-110">EXAMPLES</span></span>

## <span data-ttu-id="2acf3-111">변수</span><span class="sxs-lookup"><span data-stu-id="2acf3-111">PARAMETERS</span></span>

### <span data-ttu-id="2acf3-112">일</span><span class="sxs-lookup"><span data-stu-id="2acf3-112">-Days</span></span>
<span data-ttu-id="2acf3-113">랩의 가상 컴퓨터를 시작 해야 하는 경우의 요일을 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acf3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acf3-114">-DefaultProfile</span></span>
<span data-ttu-id="2acf3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2acf3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2acf3-116">-Disable</span><span class="sxs-lookup"><span data-stu-id="2acf3-116">-Disable</span></span>
<span data-ttu-id="2acf3-117">이 cmdlet이 랩에서 가상 컴퓨터에 대 한 정책을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acf3-118">-사용</span><span class="sxs-lookup"><span data-stu-id="2acf3-118">-Enable</span></span>
<span data-ttu-id="2acf3-119">이 cmdlet이 랩에서 가상 컴퓨터에 대 한 정책을 사용할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acf3-120">-시 이름</span><span class="sxs-lookup"><span data-stu-id="2acf3-120">-LabName</span></span>
<span data-ttu-id="2acf3-121">이 cmdlet이 자동 시작 정책을 설정 하는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="2acf3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2acf3-122">-ResourceGroupName</span></span>
<span data-ttu-id="2acf3-123">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="2acf3-124">타임</span><span class="sxs-lookup"><span data-stu-id="2acf3-124">-Time</span></span>
<span data-ttu-id="2acf3-125">랩의 가상 컴퓨터를 시작 해야 하는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acf3-126">-확인</span><span class="sxs-lookup"><span data-stu-id="2acf3-126">-Confirm</span></span>
<span data-ttu-id="2acf3-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acf3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2acf3-128">-WhatIf</span></span>
<span data-ttu-id="2acf3-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2acf3-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acf3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acf3-131">CommonParameters</span></span>
<span data-ttu-id="2acf3-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acf3-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2acf3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acf3-134">입력</span><span class="sxs-lookup"><span data-stu-id="2acf3-134">INPUTS</span></span>

### <span data-ttu-id="2acf3-135">않아야</span><span class="sxs-lookup"><span data-stu-id="2acf3-135">None</span></span>
<span data-ttu-id="2acf3-136">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2acf3-137">출력</span><span class="sxs-lookup"><span data-stu-id="2acf3-137">OUTPUTS</span></span>

### <span data-ttu-id="2acf3-138">Microsoft. DevTestLabs. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="2acf3-138">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="2acf3-139">이 cmdlet은 랩의 가상 컴퓨터를 시작 해야 하는 시기를 지정 하는 일정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2acf3-139">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="2acf3-140">상속자</span><span class="sxs-lookup"><span data-stu-id="2acf3-140">NOTES</span></span>

## <span data-ttu-id="2acf3-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2acf3-141">RELATED LINKS</span></span>

[<span data-ttu-id="2acf3-142">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="2acf3-142">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)


