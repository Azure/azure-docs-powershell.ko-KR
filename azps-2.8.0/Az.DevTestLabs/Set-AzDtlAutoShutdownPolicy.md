---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 4b15f20f9399df277fc2d2a76f7e51c2a7d57d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696603"
---
# <span data-ttu-id="922d0-101">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="922d0-101">Set-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="922d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="922d0-102">SYNOPSIS</span></span>
<span data-ttu-id="922d0-103">랩 DevTest 랩에서 자동 종료 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

## <span data-ttu-id="922d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="922d0-104">SYNTAX</span></span>

### <span data-ttu-id="922d0-105">사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="922d0-105">Enable (Default)</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922d0-106">설정할</span><span class="sxs-lookup"><span data-stu-id="922d0-106">Disable</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="922d0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="922d0-107">DESCRIPTION</span></span>
<span data-ttu-id="922d0-108">**AzDtlAutoShutdownPolicy** cmdlet은 랩에서 자동 종료 정책을 설정 하 여 지정 된 시간에 랩에서 모든 가상 컴퓨터를 자동으로 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-108">The **Set-AzDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="922d0-109">Cmdlet은 지정 된 리소스 그룹 및 랩의 이름을 사용 하 여 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="922d0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="922d0-110">EXAMPLES</span></span>

## <span data-ttu-id="922d0-111">변수</span><span class="sxs-lookup"><span data-stu-id="922d0-111">PARAMETERS</span></span>

### <span data-ttu-id="922d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922d0-112">-DefaultProfile</span></span>
<span data-ttu-id="922d0-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="922d0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="922d0-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="922d0-114">-Disable</span></span>
<span data-ttu-id="922d0-115">Cmdlet이 랩에서 정책을 사용 하지 않도록 설정 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="922d0-116">-사용</span><span class="sxs-lookup"><span data-stu-id="922d0-116">-Enable</span></span>
<span data-ttu-id="922d0-117">Cmdlet이 랩에서 정책을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="922d0-118">-시 이름</span><span class="sxs-lookup"><span data-stu-id="922d0-118">-LabName</span></span>
<span data-ttu-id="922d0-119">이 cmdlet이 자동 종료 정책을 설정 하는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="922d0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="922d0-120">-ResourceGroupName</span></span>
<span data-ttu-id="922d0-121">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="922d0-122">타임</span><span class="sxs-lookup"><span data-stu-id="922d0-122">-Time</span></span>
<span data-ttu-id="922d0-123">랩의 가상 컴퓨터를 종료 해야 하는 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

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

### <span data-ttu-id="922d0-124">-확인</span><span class="sxs-lookup"><span data-stu-id="922d0-124">-Confirm</span></span>
<span data-ttu-id="922d0-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="922d0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="922d0-126">-WhatIf</span></span>
<span data-ttu-id="922d0-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="922d0-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="922d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922d0-129">CommonParameters</span></span>
<span data-ttu-id="922d0-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922d0-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922d0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922d0-132">입력</span><span class="sxs-lookup"><span data-stu-id="922d0-132">INPUTS</span></span>

### <span data-ttu-id="922d0-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="922d0-133">System.String</span></span>

## <span data-ttu-id="922d0-134">출력</span><span class="sxs-lookup"><span data-stu-id="922d0-134">OUTPUTS</span></span>

### <span data-ttu-id="922d0-135">Microsoft. DevTestLabs. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="922d0-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="922d0-136">상속자</span><span class="sxs-lookup"><span data-stu-id="922d0-136">NOTES</span></span>

## <span data-ttu-id="922d0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="922d0-137">RELATED LINKS</span></span>

[<span data-ttu-id="922d0-138">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="922d0-138">Get-AzDtlAutoShutdownPolicy</span></span>](./Get-AzDtlAutoShutdownPolicy.md)


