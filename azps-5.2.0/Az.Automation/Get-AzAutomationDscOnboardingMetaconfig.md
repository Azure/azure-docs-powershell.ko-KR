---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 007142cb854e2e428983f95d7bb7397c5a0ace39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373871"
---
# <span data-ttu-id="9e5db-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="9e5db-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="9e5db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e5db-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5db-103">메타 구성 .mof 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="9e5db-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e5db-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e5db-105">설명</span><span class="sxs-lookup"><span data-stu-id="9e5db-105">DESCRIPTION</span></span>
<span data-ttu-id="9e5db-106">**Get-AzAutomationDscOnboardingMetaconfig** cmdlet은 APS DSC(Desired State Configuration) 메타 구성 MOF(관리 개체 형식) 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="9e5db-107">이 cmdlet은 지정한 각 컴퓨터 이름에 대해 .mof 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="9e5db-108">cmdlet은 .mof 파일에 대한 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="9e5db-109">이 폴더에 Set-DscLocalConfigurationManager cmdlet을 실행하여 이러한 컴퓨터를 DSC 노드로 Azure Automation 계정에 온보드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="9e5db-110">예제</span><span class="sxs-lookup"><span data-stu-id="9e5db-110">EXAMPLES</span></span>

### <span data-ttu-id="9e5db-111">예제 1: Automation DSC에 서버 온보드</span><span class="sxs-lookup"><span data-stu-id="9e5db-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="9e5db-112">첫 번째 명령은 Contoso17이라는 Automation 계정에 대한 두 서버에 대한 DSC 메타 구성 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="9e5db-113">이 명령은 이러한 파일을 데스크톱에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="9e5db-114">두 번째 명령은 **Set-DscLocalConfigurationManager** cmdlet을 사용하여 지정한 컴퓨터에 메타 구성을 적용하여 DSC 노드로 온보드합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="9e5db-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e5db-115">PARAMETERS</span></span>

### <span data-ttu-id="9e5db-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e5db-116">-AutomationAccountName</span></span>
<span data-ttu-id="9e5db-117">Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="9e5db-118">*ComputerName* 매개 변수가 이 매개 변수가 지정하는 계정에 지정하는 컴퓨터를 온보드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e5db-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="9e5db-119">-ComputerName</span></span>
<span data-ttu-id="9e5db-120">이 cmdlet에서 .mof 파일을 생성하는 컴퓨터의 이름 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="9e5db-121">이 매개 변수를 지정하지 않으면 cmdlet은 현재 컴퓨터(localhost)에 대한 .mof 파일을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e5db-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5db-122">-DefaultProfile</span></span>
<span data-ttu-id="9e5db-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9e5db-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e5db-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9e5db-124">-Force</span></span>
<span data-ttu-id="9e5db-125">확인 메시지를 표시하지 않고 명령을 강제로 실행하고 이름이 같은 기존 .mof 파일을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="9e5db-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="9e5db-126">-OutputFolder</span></span>
<span data-ttu-id="9e5db-127">이 cmdlet이 .mof 파일을 저장하는 폴더의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="9e5db-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e5db-128">-ResourceGroupName</span></span>
<span data-ttu-id="9e5db-129">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9e5db-130">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 컴퓨터를 온보드하는 .mof 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e5db-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e5db-131">-Confirm</span></span>
<span data-ttu-id="9e5db-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e5db-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e5db-133">-WhatIf</span></span>
<span data-ttu-id="9e5db-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9e5db-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e5db-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e5db-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5db-136">CommonParameters</span></span>
<span data-ttu-id="9e5db-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e5db-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5db-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9e5db-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5db-139">입력</span><span class="sxs-lookup"><span data-stu-id="9e5db-139">INPUTS</span></span>

### <span data-ttu-id="9e5db-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9e5db-140">System.String</span></span>

### <span data-ttu-id="9e5db-141">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9e5db-141">System.String[]</span></span>

## <span data-ttu-id="9e5db-142">출력</span><span class="sxs-lookup"><span data-stu-id="9e5db-142">OUTPUTS</span></span>

### <span data-ttu-id="9e5db-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="9e5db-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="9e5db-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e5db-144">NOTES</span></span>

## <span data-ttu-id="9e5db-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e5db-145">RELATED LINKS</span></span>
