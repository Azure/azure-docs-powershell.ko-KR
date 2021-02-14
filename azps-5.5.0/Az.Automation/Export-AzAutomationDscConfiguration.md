---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 27fbac9c368725a25845454adf044c2ff6704f3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197124"
---
# <span data-ttu-id="c5d3d-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5d3d-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="c5d3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d3d-103">Automation에서 로컬 파일로 DSC 구성을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="c5d3d-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5d3d-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5d3d-105">설명</span><span class="sxs-lookup"><span data-stu-id="c5d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d3d-106">**Export-AzAutomationDscConfiguration** cmdlet은 APS DSC(Desired State Configuration) 구성을 Azure Automation에서 로컬 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="c5d3d-107">내보낼 파일에는 .ps1 파일 이름 확장명이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="c5d3d-108">예제</span><span class="sxs-lookup"><span data-stu-id="c5d3d-108">EXAMPLES</span></span>

### <span data-ttu-id="c5d3d-109">예제 1: 게시된 버전의 DSC 구성 내보내기</span><span class="sxs-lookup"><span data-stu-id="c5d3d-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="c5d3d-110">이 명령은 Automation에서 게시된 버전의 DSC 구성을 데스크톱인 지정된 폴더로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="c5d3d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5d3d-111">PARAMETERS</span></span>

### <span data-ttu-id="c5d3d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c5d3d-112">-AutomationAccountName</span></span>
<span data-ttu-id="c5d3d-113">이 cmdlet에서 내보낼 DSC를 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="c5d3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d3d-114">-DefaultProfile</span></span>
<span data-ttu-id="c5d3d-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c5d3d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5d3d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c5d3d-116">-Force</span></span>
<span data-ttu-id="c5d3d-117">이 cmdlet이 기존 로컬 파일을 이름이 같은 새 파일로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="c5d3d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c5d3d-118">-Name</span></span>
<span data-ttu-id="c5d3d-119">이 cmdlet에서 내보낼 DSC 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d3d-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="c5d3d-120">-OutputFolder</span></span>
<span data-ttu-id="c5d3d-121">이 cmdlet이 DSC 구성을 내보낼 출력 폴더를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="c5d3d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d3d-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5d3d-123">이 cmdlet이 DSC 구성을 내보낼 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="c5d3d-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="c5d3d-124">-Slot</span></span>
<span data-ttu-id="c5d3d-125">이 cmdlet에서 내보낼 DSC 구성의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="c5d3d-126">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="c5d3d-126">Valid values are:</span></span> 
- <span data-ttu-id="c5d3d-127">초안</span><span class="sxs-lookup"><span data-stu-id="c5d3d-127">Draft</span></span>
- <span data-ttu-id="c5d3d-128">게시된 기본값은 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d3d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5d3d-129">-Confirm</span></span>
<span data-ttu-id="c5d3d-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5d3d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5d3d-131">-WhatIf</span></span>
<span data-ttu-id="c5d3d-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c5d3d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5d3d-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5d3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d3d-134">CommonParameters</span></span>
<span data-ttu-id="c5d3d-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d3d-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c5d3d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d3d-137">입력</span><span class="sxs-lookup"><span data-stu-id="c5d3d-137">INPUTS</span></span>

### <span data-ttu-id="c5d3d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c5d3d-138">System.String</span></span>

## <span data-ttu-id="c5d3d-139">출력</span><span class="sxs-lookup"><span data-stu-id="c5d3d-139">OUTPUTS</span></span>

### <span data-ttu-id="c5d3d-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="c5d3d-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="c5d3d-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5d3d-141">NOTES</span></span>

## <span data-ttu-id="c5d3d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5d3d-142">RELATED LINKS</span></span>

[<span data-ttu-id="c5d3d-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5d3d-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="c5d3d-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5d3d-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


