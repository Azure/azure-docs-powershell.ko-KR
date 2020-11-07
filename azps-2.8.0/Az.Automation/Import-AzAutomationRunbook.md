---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: 9ec19ee8e1e6a74de83f77b8dca4e2536af8e425
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697808"
---
# <span data-ttu-id="d0c51-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c51-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="d0c51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0c51-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c51-103">자동화 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="d0c51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0c51-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0c51-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d0c51-105">DESCRIPTION</span></span>
<span data-ttu-id="d0c51-106">**AzAutomationRunbook** Cmdlet은 Azure Automation runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="d0c51-107">Wps_2에 대해 가져올 wps_2 스크립트 (ps1) 파일에 대 한 경로를 지정 하 고, 그래픽 runbook의 wps_2 워크플로 runbook 또는 python 2 runbook의 경우 (py) 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="d0c51-108">Wps_2 워크플로 runbook의 경우 스크립트에는 파일 이름과 일치 하는 단일 wps_2 워크플로 정의가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="d0c51-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d0c51-109">EXAMPLES</span></span>

### <span data-ttu-id="d0c51-110">예제 1: 파일에서 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="d0c51-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="d0c51-111">첫 번째 명령은 두 개의 키/값 쌍을 $Tags 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="d0c51-112">두 번째 명령은 GraphicalRunbook06 이라는 그래픽 runbook을 AutomationAccount01 이라는 Automation 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="d0c51-113">또한이 명령은 $Tags에 저장 된 태그를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="d0c51-114">변수</span><span class="sxs-lookup"><span data-stu-id="d0c51-114">PARAMETERS</span></span>

### <span data-ttu-id="d0c51-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d0c51-115">-AutomationAccountName</span></span>
<span data-ttu-id="d0c51-116">이 cmdlet이 runbook을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="d0c51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c51-117">-DefaultProfile</span></span>
<span data-ttu-id="d0c51-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d0c51-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0c51-119">-설명</span><span class="sxs-lookup"><span data-stu-id="d0c51-119">-Description</span></span>
<span data-ttu-id="d0c51-120">가져온 runbook에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-120">Specifies a description for the imported runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c51-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d0c51-121">-Force</span></span>
<span data-ttu-id="d0c51-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="d0c51-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c51-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="d0c51-123">-LogProgress</span></span>
<span data-ttu-id="d0c51-124">Runbook이 진행률 정보를 기록 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c51-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="d0c51-125">-LogVerbose</span></span>
<span data-ttu-id="d0c51-126">Runbook이 자세한 정보를 기록 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c51-127">-이름</span><span class="sxs-lookup"><span data-stu-id="d0c51-127">-Name</span></span>
<span data-ttu-id="d0c51-128">이 cmdlet이 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c51-129">-Path</span><span class="sxs-lookup"><span data-stu-id="d0c51-129">-Path</span></span>
<span data-ttu-id="d0c51-130">이 cmdlet이 가져온 ps1 또는 graphrunbook 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c51-131">게시 됨</span><span class="sxs-lookup"><span data-stu-id="d0c51-131">-Published</span></span>
<span data-ttu-id="d0c51-132">이 cmdlet이 가져오는 runbook을 게시 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c51-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0c51-133">-ResourceGroupName</span></span>
<span data-ttu-id="d0c51-134">이 cmdlet이 runbook을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="d0c51-135">태그</span><span class="sxs-lookup"><span data-stu-id="d0c51-135">-Tags</span></span>
<span data-ttu-id="d0c51-136">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d0c51-137">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d0c51-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c51-138">-Type</span><span class="sxs-lookup"><span data-stu-id="d0c51-138">-Type</span></span>
<span data-ttu-id="d0c51-139">이 cmdlet이 만드는 runbook의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="d0c51-140">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-140">Valid values are:</span></span>
- <span data-ttu-id="d0c51-141">슬래시</span><span class="sxs-lookup"><span data-stu-id="d0c51-141">PowerShell</span></span>
- <span data-ttu-id="d0c51-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="d0c51-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="d0c51-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="d0c51-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="d0c51-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="d0c51-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="d0c51-145">Graph</span><span class="sxs-lookup"><span data-stu-id="d0c51-145">Graph</span></span>
- <span data-ttu-id="d0c51-146">Python2 값 그래프는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="d0c51-147">이는 GraphicalPowerShellWorkflow와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c51-148">-확인</span><span class="sxs-lookup"><span data-stu-id="d0c51-148">-Confirm</span></span>
<span data-ttu-id="d0c51-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0c51-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0c51-150">-WhatIf</span></span>
<span data-ttu-id="d0c51-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0c51-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0c51-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c51-153">CommonParameters</span></span>
<span data-ttu-id="d0c51-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0c51-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c51-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0c51-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c51-156">입력</span><span class="sxs-lookup"><span data-stu-id="d0c51-156">INPUTS</span></span>

### <span data-ttu-id="d0c51-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d0c51-157">System.String</span></span>

### <span data-ttu-id="d0c51-158">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="d0c51-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="d0c51-159">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d0c51-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d0c51-160">출력</span><span class="sxs-lookup"><span data-stu-id="d0c51-160">OUTPUTS</span></span>

### <span data-ttu-id="d0c51-161">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="d0c51-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="d0c51-162">상속자</span><span class="sxs-lookup"><span data-stu-id="d0c51-162">NOTES</span></span>

## <span data-ttu-id="d0c51-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0c51-163">RELATED LINKS</span></span>

[<span data-ttu-id="d0c51-164">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c51-164">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="d0c51-165">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c51-165">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="d0c51-166">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c51-166">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d0c51-167">게시-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c51-167">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="d0c51-168">제거-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c51-168">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="d0c51-169">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c51-169">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="d0c51-170">시작-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d0c51-170">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
