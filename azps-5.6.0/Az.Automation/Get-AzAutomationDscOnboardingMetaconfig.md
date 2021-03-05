---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: e520fec3d0299ca2b5f74bb2a8a8b7de437d7a2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008155"
---
# <span data-ttu-id="bd4d3-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="bd4d3-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="bd4d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="bd4d3-103">메타 구성 .mof 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="bd4d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd4d3-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd4d3-105">설명</span><span class="sxs-lookup"><span data-stu-id="bd4d3-105">DESCRIPTION</span></span>
<span data-ttu-id="bd4d3-106">**Get-AzAutomationDscOnboardingMetaconfig** cmdlet은 APS 원하는 상태 구성(DSC) 메타 구성 관리 개체 형식(MOF) 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="bd4d3-107">이 cmdlet은 지정한 각 컴퓨터 이름에 대해 .mof 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="bd4d3-108">cmdlet은 .mof 파일에 대한 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="bd4d3-109">이 폴더의 Set-DscLocalConfigurationManager cmdlet을 실행하여 이러한 컴퓨터를 DSC 노드로 Azure Automation 계정에 온보드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="bd4d3-110">예제</span><span class="sxs-lookup"><span data-stu-id="bd4d3-110">EXAMPLES</span></span>

### <span data-ttu-id="bd4d3-111">예제 1: Automation DSC에 서버 온보드</span><span class="sxs-lookup"><span data-stu-id="bd4d3-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="bd4d3-112">첫 번째 명령은 Contoso17이라는 Automation 계정의 두 서버에 대해 DSC 메타 구성 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="bd4d3-113">명령은 데스크톱에 이러한 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="bd4d3-114">두 번째 명령은 **Set-DscLocalConfigurationManager** cmdlet을 사용하여 지정된 컴퓨터에 메타 구성을 적용하여 DSC 노드로 온보드합니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="bd4d3-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bd4d3-115">PARAMETERS</span></span>

### <span data-ttu-id="bd4d3-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bd4d3-116">-AutomationAccountName</span></span>
<span data-ttu-id="bd4d3-117">Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="bd4d3-118">*ComputerName* 매개 변수가 이 매개 변수가 지정하는 계정에 지정하는 컴퓨터를 온보드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="bd4d3-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="bd4d3-119">-ComputerName</span></span>
<span data-ttu-id="bd4d3-120">이 cmdlet에서 .mof 파일을 생성하는 컴퓨터의 이름 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="bd4d3-121">이 매개 변수를 지정하지 않으면 cmdlet은 현재 컴퓨터(localhost)에 대한 .mof 파일을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

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

### <span data-ttu-id="bd4d3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd4d3-122">-DefaultProfile</span></span>
<span data-ttu-id="bd4d3-123">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bd4d3-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd4d3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bd4d3-124">-Force</span></span>
<span data-ttu-id="bd4d3-125">확인을 묻는 메시지를 표시하지 않고 명령을 강제로 실행하고 이름이 동일한 기존 .mof 파일을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="bd4d3-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="bd4d3-126">-OutputFolder</span></span>
<span data-ttu-id="bd4d3-127">이 cmdlet에서 .mof 파일을 저장하는 폴더의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="bd4d3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd4d3-128">-ResourceGroupName</span></span>
<span data-ttu-id="bd4d3-129">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bd4d3-130">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 컴퓨터에 온보드할 .mof 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bd4d3-131">-확인</span><span class="sxs-lookup"><span data-stu-id="bd4d3-131">-Confirm</span></span>
<span data-ttu-id="bd4d3-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd4d3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd4d3-133">-WhatIf</span></span>
<span data-ttu-id="bd4d3-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd4d3-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd4d3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd4d3-136">CommonParameters</span></span>
<span data-ttu-id="bd4d3-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd4d3-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd4d3-139">입력</span><span class="sxs-lookup"><span data-stu-id="bd4d3-139">INPUTS</span></span>

### <span data-ttu-id="bd4d3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bd4d3-140">System.String</span></span>

### <span data-ttu-id="bd4d3-141">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bd4d3-141">System.String[]</span></span>

## <span data-ttu-id="bd4d3-142">출력</span><span class="sxs-lookup"><span data-stu-id="bd4d3-142">OUTPUTS</span></span>

### <span data-ttu-id="bd4d3-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="bd4d3-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="bd4d3-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd4d3-144">NOTES</span></span>

## <span data-ttu-id="bd4d3-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd4d3-145">RELATED LINKS</span></span>
