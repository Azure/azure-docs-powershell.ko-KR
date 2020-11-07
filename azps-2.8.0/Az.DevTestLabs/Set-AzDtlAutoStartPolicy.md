---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
ms.openlocfilehash: c751335f05f0e6ac9df5acb585dc5eb651d957a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696604"
---
# <span data-ttu-id="41970-101">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="41970-101">Set-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="41970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41970-102">SYNOPSIS</span></span>
<span data-ttu-id="41970-103">DevTest 랩에서 랩에서 자동 시작 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="41970-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41970-104">SYNTAX</span></span>

### <span data-ttu-id="41970-105">사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="41970-105">Enable (Default)</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41970-106">설정할</span><span class="sxs-lookup"><span data-stu-id="41970-106">Disable</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41970-107">설명은</span><span class="sxs-lookup"><span data-stu-id="41970-107">DESCRIPTION</span></span>
<span data-ttu-id="41970-108">**AzDtlAutoStartPolicy** cmdlet은 랩의 자동 시작 정책을 설정 하 여 랩 가상 컴퓨터에 자동 시작을 예약할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-108">The **Set-AzDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="41970-109">Cmdlet은 지정 된 리소스 그룹 및 랩의 이름을 사용 하 여 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="41970-110">예제의</span><span class="sxs-lookup"><span data-stu-id="41970-110">EXAMPLES</span></span>

## <span data-ttu-id="41970-111">변수</span><span class="sxs-lookup"><span data-stu-id="41970-111">PARAMETERS</span></span>

### <span data-ttu-id="41970-112">일</span><span class="sxs-lookup"><span data-stu-id="41970-112">-Days</span></span>
<span data-ttu-id="41970-113">랩의 가상 컴퓨터를 시작 해야 하는 경우의 요일을 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41970-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41970-114">-DefaultProfile</span></span>
<span data-ttu-id="41970-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="41970-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41970-116">-Disable</span><span class="sxs-lookup"><span data-stu-id="41970-116">-Disable</span></span>
<span data-ttu-id="41970-117">이 cmdlet이 랩에서 가상 컴퓨터에 대 한 정책을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41970-118">-사용</span><span class="sxs-lookup"><span data-stu-id="41970-118">-Enable</span></span>
<span data-ttu-id="41970-119">이 cmdlet이 랩에서 가상 컴퓨터에 대 한 정책을 사용할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41970-120">-시 이름</span><span class="sxs-lookup"><span data-stu-id="41970-120">-LabName</span></span>
<span data-ttu-id="41970-121">이 cmdlet이 자동 시작 정책을 설정 하는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="41970-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41970-122">-ResourceGroupName</span></span>
<span data-ttu-id="41970-123">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="41970-124">타임</span><span class="sxs-lookup"><span data-stu-id="41970-124">-Time</span></span>
<span data-ttu-id="41970-125">랩의 가상 컴퓨터를 시작 해야 하는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41970-126">-확인</span><span class="sxs-lookup"><span data-stu-id="41970-126">-Confirm</span></span>
<span data-ttu-id="41970-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41970-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41970-128">-WhatIf</span></span>
<span data-ttu-id="41970-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41970-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41970-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41970-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41970-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41970-131">CommonParameters</span></span>
<span data-ttu-id="41970-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41970-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41970-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41970-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41970-134">입력</span><span class="sxs-lookup"><span data-stu-id="41970-134">INPUTS</span></span>

### <span data-ttu-id="41970-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41970-135">System.String</span></span>

## <span data-ttu-id="41970-136">출력</span><span class="sxs-lookup"><span data-stu-id="41970-136">OUTPUTS</span></span>

### <span data-ttu-id="41970-137">Microsoft. DevTestLabs. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="41970-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="41970-138">상속자</span><span class="sxs-lookup"><span data-stu-id="41970-138">NOTES</span></span>

## <span data-ttu-id="41970-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41970-139">RELATED LINKS</span></span>

[<span data-ttu-id="41970-140">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="41970-140">Get-AzDtlAutoStartPolicy</span></span>](./Get-AzDtlAutoStartPolicy.md)

