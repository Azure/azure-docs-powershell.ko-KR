---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 34dcb85de9520882b9202edd38ae2e44d1bcafee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711211"
---
# <span data-ttu-id="067c4-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="067c4-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="067c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="067c4-102">SYNOPSIS</span></span>
<span data-ttu-id="067c4-103">메타 구성 .mof 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-103">Creates meta-configuration .mof files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="067c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="067c4-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="067c4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="067c4-105">DESCRIPTION</span></span>
<span data-ttu-id="067c4-106">**AzureRmAutomationDscOnboardingMetaconfig** CMDLET은 DSC (원하는 상태 구성) 메타 구성 관리 개체 형식 (MOF) 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-106">The **Get-AzureRmAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="067c4-107">이 cmdlet은 사용자가 지정 하는 각 컴퓨터 이름에 대 한 .mof 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="067c4-108">Cmdlet은 .mof 파일에 대 한 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="067c4-109">이 폴더에 대 한 Set-DscLocalConfigurationManager cmdlet을 실행 하 여 이러한 컴퓨터를 DSC 노드로 Azure Automation 계정으로 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="067c4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="067c4-110">EXAMPLES</span></span>

### <span data-ttu-id="067c4-111">예제 1: 자동화 DSC에 대 한 온보드 서버</span><span class="sxs-lookup"><span data-stu-id="067c4-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="067c4-112">첫 번째 명령은 Contoso17 이라는 자동화 계정에 대 한 두 서버에 대해 DSC 메타 구성 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="067c4-113">이 명령은 바탕 화면에 이러한 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-113">The command saves these files on a desktop.</span></span>

<span data-ttu-id="067c4-114">두 번째 명령은 **Set-DscLocalConfigurationManager** cmdlet을 사용 하 여 지정 된 컴퓨터에 meta 구성을 적용 하 여 DSC 노드로 내장 합니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="067c4-115">변수</span><span class="sxs-lookup"><span data-stu-id="067c4-115">PARAMETERS</span></span>

### <span data-ttu-id="067c4-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="067c4-116">-AutomationAccountName</span></span>
<span data-ttu-id="067c4-117">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="067c4-118">*ComputerName* 매개 변수에서 지정 하는 컴퓨터를이 매개 변수에서 지정 하는 계정에 온보드 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="067c4-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="067c4-119">-ComputerName</span></span>
<span data-ttu-id="067c4-120">이 cmdlet이 .mof 파일을 생성 하는 컴퓨터의 이름 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="067c4-121">이 매개 변수를 지정 하지 않으면 cmdlet에서 현재 컴퓨터 (localhost)에 대 한 .mof 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="067c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="067c4-122">-DefaultProfile</span></span>
<span data-ttu-id="067c4-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="067c4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="067c4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="067c4-124">-Force</span></span>
<span data-ttu-id="067c4-125">확인 메시지를 표시 하지 않고 명령을 강제로 실행 하 고 동일한 이름을 가진 기존 .mof 파일을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="067c4-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="067c4-126">-OutputFolder</span></span>
<span data-ttu-id="067c4-127">이 cmdlet에서 .mof 파일을 저장 하는 폴더의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="067c4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="067c4-128">-ResourceGroupName</span></span>
<span data-ttu-id="067c4-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="067c4-130">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 온보드 컴퓨터로 .mof 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="067c4-131">-확인</span><span class="sxs-lookup"><span data-stu-id="067c4-131">-Confirm</span></span>
<span data-ttu-id="067c4-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="067c4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="067c4-133">-WhatIf</span></span>
<span data-ttu-id="067c4-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="067c4-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="067c4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="067c4-136">CommonParameters</span></span>
<span data-ttu-id="067c4-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="067c4-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="067c4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="067c4-139">입력</span><span class="sxs-lookup"><span data-stu-id="067c4-139">INPUTS</span></span>

### <span data-ttu-id="067c4-140">않아야</span><span class="sxs-lookup"><span data-stu-id="067c4-140">None</span></span>
<span data-ttu-id="067c4-141">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="067c4-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="067c4-142">출력</span><span class="sxs-lookup"><span data-stu-id="067c4-142">OUTPUTS</span></span>

### <span data-ttu-id="067c4-143">DscOnboardingMetaconfig를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="067c4-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="067c4-144">상속자</span><span class="sxs-lookup"><span data-stu-id="067c4-144">NOTES</span></span>

## <span data-ttu-id="067c4-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="067c4-145">RELATED LINKS</span></span>

