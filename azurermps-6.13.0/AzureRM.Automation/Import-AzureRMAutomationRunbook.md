---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: f6399c35316deb5590eada9eccd474ba7e47b116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531494"
---
# <span data-ttu-id="11ac7-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11ac7-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="11ac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="11ac7-103">자동화 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11ac7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11ac7-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11ac7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11ac7-105">DESCRIPTION</span></span>
<span data-ttu-id="11ac7-106">**AzureRmAutomationRunbook** Cmdlet은 Azure Automation runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="11ac7-107">Wps_2에 대해 가져올 wps_2 스크립트 (ps1) 파일에 대 한 경로를 지정 하 고, 그래픽 runbook의 wps_2 워크플로 runbook 또는 python 2 runbook의 경우 (py) 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="11ac7-108">Wps_2 워크플로 runbook의 경우 스크립트에는 파일 이름과 일치 하는 단일 wps_2 워크플로 정의가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="11ac7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="11ac7-109">EXAMPLES</span></span>

### <span data-ttu-id="11ac7-110">예제 1: 파일에서 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="11ac7-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="11ac7-111">첫 번째 명령은 두 개의 키/값 쌍을 $Tags 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="11ac7-112">두 번째 명령은 GraphicalRunbook06 이라는 그래픽 runbook을 AutomationAccount01 이라는 Automation 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="11ac7-113">또한이 명령은 $Tags에 저장 된 태그를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="11ac7-114">변수</span><span class="sxs-lookup"><span data-stu-id="11ac7-114">PARAMETERS</span></span>

### <span data-ttu-id="11ac7-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11ac7-115">-AutomationAccountName</span></span>
<span data-ttu-id="11ac7-116">이 cmdlet이 runbook을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="11ac7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ac7-117">-DefaultProfile</span></span>
<span data-ttu-id="11ac7-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="11ac7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ac7-119">-설명</span><span class="sxs-lookup"><span data-stu-id="11ac7-119">-Description</span></span>
<span data-ttu-id="11ac7-120">가져온 runbook에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="11ac7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="11ac7-121">-Force</span></span>
<span data-ttu-id="11ac7-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="11ac7-122">ps_force</span></span>

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

### <span data-ttu-id="11ac7-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="11ac7-123">-LogProgress</span></span>
<span data-ttu-id="11ac7-124">Runbook이 진행률 정보를 기록 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="11ac7-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="11ac7-125">-LogVerbose</span></span>
<span data-ttu-id="11ac7-126">Runbook이 자세한 정보를 기록 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="11ac7-127">-이름</span><span class="sxs-lookup"><span data-stu-id="11ac7-127">-Name</span></span>
<span data-ttu-id="11ac7-128">이 cmdlet이 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="11ac7-129">-Path</span><span class="sxs-lookup"><span data-stu-id="11ac7-129">-Path</span></span>
<span data-ttu-id="11ac7-130">이 cmdlet이 가져온 ps1 또는 graphrunbook 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="11ac7-131">게시 됨</span><span class="sxs-lookup"><span data-stu-id="11ac7-131">-Published</span></span>
<span data-ttu-id="11ac7-132">이 cmdlet이 가져오는 runbook을 게시 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="11ac7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ac7-133">-ResourceGroupName</span></span>
<span data-ttu-id="11ac7-134">이 cmdlet이 runbook을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="11ac7-135">태그</span><span class="sxs-lookup"><span data-stu-id="11ac7-135">-Tags</span></span>
<span data-ttu-id="11ac7-136">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="11ac7-137">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="11ac7-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="11ac7-138">-Type</span><span class="sxs-lookup"><span data-stu-id="11ac7-138">-Type</span></span>
<span data-ttu-id="11ac7-139">이 cmdlet이 만드는 runbook의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="11ac7-140">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-140">Valid values are:</span></span>
- <span data-ttu-id="11ac7-141">슬래시</span><span class="sxs-lookup"><span data-stu-id="11ac7-141">PowerShell</span></span>
- <span data-ttu-id="11ac7-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="11ac7-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="11ac7-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="11ac7-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="11ac7-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="11ac7-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="11ac7-145">Graph</span><span class="sxs-lookup"><span data-stu-id="11ac7-145">Graph</span></span>
- <span data-ttu-id="11ac7-146">Python2 값 그래프는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="11ac7-147">이는 GraphicalPowerShellWorkflow와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="11ac7-148">-확인</span><span class="sxs-lookup"><span data-stu-id="11ac7-148">-Confirm</span></span>
<span data-ttu-id="11ac7-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ac7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ac7-150">-WhatIf</span></span>
<span data-ttu-id="11ac7-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11ac7-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ac7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ac7-153">CommonParameters</span></span>
<span data-ttu-id="11ac7-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ac7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ac7-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ac7-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ac7-156">입력</span><span class="sxs-lookup"><span data-stu-id="11ac7-156">INPUTS</span></span>

### <span data-ttu-id="11ac7-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11ac7-157">System.String</span></span>

### <span data-ttu-id="11ac7-158">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="11ac7-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="11ac7-159">시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="11ac7-159">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="11ac7-160">출력</span><span class="sxs-lookup"><span data-stu-id="11ac7-160">OUTPUTS</span></span>

### <span data-ttu-id="11ac7-161">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="11ac7-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="11ac7-162">상속자</span><span class="sxs-lookup"><span data-stu-id="11ac7-162">NOTES</span></span>

## <span data-ttu-id="11ac7-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11ac7-163">RELATED LINKS</span></span>

[<span data-ttu-id="11ac7-164">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11ac7-164">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="11ac7-165">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11ac7-165">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="11ac7-166">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11ac7-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="11ac7-167">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11ac7-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="11ac7-168">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11ac7-168">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="11ac7-169">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11ac7-169">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="11ac7-170">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11ac7-170">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="11ac7-171">시작-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11ac7-171">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
