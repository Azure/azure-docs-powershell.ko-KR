---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3680d277addba29444f3f2955d7cca28505435a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014043"
---
# <span data-ttu-id="672a6-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="672a6-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="672a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="672a6-102">SYNOPSIS</span></span>
<span data-ttu-id="672a6-103">Automation에서 MOF 문서를 DSC 노드 구성으로 가져온다.</span><span class="sxs-lookup"><span data-stu-id="672a6-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="672a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="672a6-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="672a6-105">설명</span><span class="sxs-lookup"><span data-stu-id="672a6-105">DESCRIPTION</span></span>
<span data-ttu-id="672a6-106">**Import-AzAutomationDscConfiguration** cmdlet은 MOF(관리 개체 형식) 구성 문서를 Azure Automation에 DSC(원하는 상태 구성) 노드 구성으로 가져온다.</span><span class="sxs-lookup"><span data-stu-id="672a6-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="672a6-107">.mof 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="672a6-108">예제</span><span class="sxs-lookup"><span data-stu-id="672a6-108">EXAMPLES</span></span>

### <span data-ttu-id="672a6-109">예제 1: DSC 노드 구성을 Automation으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="672a6-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="672a6-110">이 명령은 Webserver.mof라는 파일에서 DSC 노드 구성을 DSC 구성 ContosoConfiguration 아래에서 Contoso17이라는 Automation 계정으로 가져온다.</span><span class="sxs-lookup"><span data-stu-id="672a6-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="672a6-111">명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="672a6-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="672a6-112">ContosoConfiguration.webserver라는 기존 DSC 노드 구성이 있는 경우 이 명령이 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="672a6-113">예제 2: DSC 노드 구성을 Automation로 가져오고 기존 NodeConfiguration을 덮어 덮어넣지 말고 새 빌드 버전을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="672a6-114">이 명령은 Webserver.mof라는 파일에서 DSC 노드 구성을 DSC 구성 ContosoConfiguration 아래에서 Contoso17이라는 Automation 계정으로 가져온다.</span><span class="sxs-lookup"><span data-stu-id="672a6-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="672a6-115">명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="672a6-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="672a6-116">ContosoConfiguration.webserver라는 기존 DSC 노드 구성이 있는 경우 이 명령은 ContosoConfiguration[2].webserver라는 이름으로 새 빌드 버전을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="672a6-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="672a6-117">PARAMETERS</span></span>

### <span data-ttu-id="672a6-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="672a6-118">-AutomationAccountName</span></span>
<span data-ttu-id="672a6-119">이 cmdlet에서 DSC 노드 구성을 가져오는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="672a6-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="672a6-120">-ConfigurationName</span></span>
<span data-ttu-id="672a6-121">가져올 노드 구성의 네임스페이스 및 컨테이너로 사용할 Automation의 DSC 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="672a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672a6-122">-DefaultProfile</span></span>
<span data-ttu-id="672a6-123">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="672a6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="672a6-124">-Force</span><span class="sxs-lookup"><span data-stu-id="672a6-124">-Force</span></span>
<span data-ttu-id="672a6-125">이 cmdlet은 Automation의 기존 DSC 노드 구성을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="672a6-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="672a6-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="672a6-127">새 노드 구성 빌드 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-127">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="672a6-128">-Path</span><span class="sxs-lookup"><span data-stu-id="672a6-128">-Path</span></span>
<span data-ttu-id="672a6-129">이 cmdlet에서 가져오는 MOF 구성 문서의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="672a6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672a6-130">-ResourceGroupName</span></span>
<span data-ttu-id="672a6-131">이 cmdlet에서 DSC 노드 구성을 가져오는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="672a6-132">-확인</span><span class="sxs-lookup"><span data-stu-id="672a6-132">-Confirm</span></span>
<span data-ttu-id="672a6-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="672a6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="672a6-134">-WhatIf</span></span>
<span data-ttu-id="672a6-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="672a6-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="672a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672a6-137">CommonParameters</span></span>
<span data-ttu-id="672a6-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="672a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672a6-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="672a6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672a6-140">입력</span><span class="sxs-lookup"><span data-stu-id="672a6-140">INPUTS</span></span>

### <span data-ttu-id="672a6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="672a6-141">System.String</span></span>

## <span data-ttu-id="672a6-142">출력</span><span class="sxs-lookup"><span data-stu-id="672a6-142">OUTPUTS</span></span>

### <span data-ttu-id="672a6-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="672a6-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="672a6-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="672a6-144">NOTES</span></span>

## <span data-ttu-id="672a6-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="672a6-145">RELATED LINKS</span></span>

[<span data-ttu-id="672a6-146">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="672a6-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="672a6-147">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="672a6-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)


