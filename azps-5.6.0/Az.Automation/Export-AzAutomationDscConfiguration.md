---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: c27f878d2dbb0e52a16216a2158c737bc523c932
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959035"
---
# <span data-ttu-id="c2d6a-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2d6a-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="c2d6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d6a-103">Automation에서 로컬 파일로 DSC 구성을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="c2d6a-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2d6a-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2d6a-105">설명</span><span class="sxs-lookup"><span data-stu-id="c2d6a-105">DESCRIPTION</span></span>
<span data-ttu-id="c2d6a-106">**Export-AzAutomationDscConfiguration** cmdlet은 Azure Automation에서 로컬 파일로 APS 원하는 상태 구성(DSC) 구성을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="c2d6a-107">내보낼 파일에 .ps1 파일 이름 확장이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="c2d6a-108">예제</span><span class="sxs-lookup"><span data-stu-id="c2d6a-108">EXAMPLES</span></span>

### <span data-ttu-id="c2d6a-109">예제 1: 게시된 버전의 DSC 구성 내보내기</span><span class="sxs-lookup"><span data-stu-id="c2d6a-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="c2d6a-110">이 명령은 Automation에서 게시된 버전의 DSC 구성을 데스크톱인 지정된 폴더로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="c2d6a-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2d6a-111">PARAMETERS</span></span>

### <span data-ttu-id="c2d6a-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c2d6a-112">-AutomationAccountName</span></span>
<span data-ttu-id="c2d6a-113">이 cmdlet에서 내보내는 DSC를 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="c2d6a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d6a-114">-DefaultProfile</span></span>
<span data-ttu-id="c2d6a-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c2d6a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2d6a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c2d6a-116">-Force</span></span>
<span data-ttu-id="c2d6a-117">이 cmdlet은 기존 로컬 파일을 동일한 이름이 있는 새 파일로 바칭합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="c2d6a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c2d6a-118">-Name</span></span>
<span data-ttu-id="c2d6a-119">이 cmdlet에서 내보내는 DSC 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="c2d6a-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="c2d6a-120">-OutputFolder</span></span>
<span data-ttu-id="c2d6a-121">이 cmdlet이 DSC 구성을 내보낼 출력 폴더를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="c2d6a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2d6a-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2d6a-123">이 cmdlet에서 DSC 구성을 내보낼 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="c2d6a-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="c2d6a-124">-Slot</span></span>
<span data-ttu-id="c2d6a-125">이 cmdlet에서 내보내는 DSC 구성의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="c2d6a-126">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="c2d6a-126">Valid values are:</span></span> 
- <span data-ttu-id="c2d6a-127">초안</span><span class="sxs-lookup"><span data-stu-id="c2d6a-127">Draft</span></span>
- <span data-ttu-id="c2d6a-128">게시된 기본값은 게시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="c2d6a-129">-확인</span><span class="sxs-lookup"><span data-stu-id="c2d6a-129">-Confirm</span></span>
<span data-ttu-id="c2d6a-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2d6a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2d6a-131">-WhatIf</span></span>
<span data-ttu-id="c2d6a-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2d6a-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2d6a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d6a-134">CommonParameters</span></span>
<span data-ttu-id="c2d6a-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d6a-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c2d6a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d6a-137">입력</span><span class="sxs-lookup"><span data-stu-id="c2d6a-137">INPUTS</span></span>

### <span data-ttu-id="c2d6a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c2d6a-138">System.String</span></span>

## <span data-ttu-id="c2d6a-139">출력</span><span class="sxs-lookup"><span data-stu-id="c2d6a-139">OUTPUTS</span></span>

### <span data-ttu-id="c2d6a-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="c2d6a-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="c2d6a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2d6a-141">NOTES</span></span>

## <span data-ttu-id="c2d6a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2d6a-142">RELATED LINKS</span></span>

[<span data-ttu-id="c2d6a-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2d6a-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="c2d6a-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2d6a-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


