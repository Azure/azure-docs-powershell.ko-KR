---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 49cd2fdb2d482621ea52f1df88c9bcd95521badd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533444"
---
# <span data-ttu-id="9a97d-101">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a97d-101">Import-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="9a97d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a97d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a97d-103">MOF 문서를 자동화의 DSC 노드 구성으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a97d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a97d-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a97d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9a97d-105">DESCRIPTION</span></span>
<span data-ttu-id="9a97d-106">**AzureRmAutomationDscConfiguration** CMDLET은 MOF (관리 개체 형식) 구성 문서를 DSC (원하는 상태 구성) 노드 구성으로 Azure 자동화로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="9a97d-107">.Mof 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="9a97d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9a97d-108">EXAMPLES</span></span>

### <span data-ttu-id="9a97d-109">예제 1: DSC 노드 구성을 자동화로 가져오기</span><span class="sxs-lookup"><span data-stu-id="9a97d-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="9a97d-110">이 명령은 Contoso17 이라는 파일의 DSC 노드 구성을 DSC 구성 ContosoConfiguration 아래의 Automation 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="9a97d-111">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9a97d-112">ContosoConfiguration 이라는 기존 DSC 노드 구성이 있는 경우이 명령은 해당 구성을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="9a97d-113">예제 2: DSC 노드 구성을 자동화로 가져오고 새 빌드 버전을 만들고 기존 NodeConfiguration 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="9a97d-114">이 명령은 Contoso17 이라는 파일의 DSC 노드 구성을 DSC 구성 ContosoConfiguration 아래의 Automation 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="9a97d-115">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9a97d-116">ContosoConfiguration 이라는 기존 DSC 노드 구성이 있는 경우이 명령은 ContosoConfiguration [2]. e 1. 라는 이름의 새 빌드 버전을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="9a97d-117">변수</span><span class="sxs-lookup"><span data-stu-id="9a97d-117">PARAMETERS</span></span>

### <span data-ttu-id="9a97d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a97d-118">-AutomationAccountName</span></span>
<span data-ttu-id="9a97d-119">이 cmdlet이 DSC 노드 구성을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="9a97d-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9a97d-120">-ConfigurationName</span></span>
<span data-ttu-id="9a97d-121">가져올 노드 구성의 네임 스페이스 및 컨테이너로 사용 하는 자동화에서 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="9a97d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a97d-122">-DefaultProfile</span></span>
<span data-ttu-id="9a97d-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9a97d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a97d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9a97d-124">-Force</span></span>
<span data-ttu-id="9a97d-125">이 cmdlet이 자동화의 기존 DSC 노드 구성을 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="9a97d-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="9a97d-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="9a97d-127">새 노드 구성 빌드 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-127">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="9a97d-128">-Path</span><span class="sxs-lookup"><span data-stu-id="9a97d-128">-Path</span></span>
<span data-ttu-id="9a97d-129">이 cmdlet이 가져오는 MOF 구성 문서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="9a97d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a97d-130">-ResourceGroupName</span></span>
<span data-ttu-id="9a97d-131">이 cmdlet이 DSC 노드 구성을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="9a97d-132">-확인</span><span class="sxs-lookup"><span data-stu-id="9a97d-132">-Confirm</span></span>
<span data-ttu-id="9a97d-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a97d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a97d-134">-WhatIf</span></span>
<span data-ttu-id="9a97d-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a97d-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a97d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a97d-137">CommonParameters</span></span>
<span data-ttu-id="9a97d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a97d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a97d-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a97d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a97d-140">입력</span><span class="sxs-lookup"><span data-stu-id="9a97d-140">INPUTS</span></span>

### <span data-ttu-id="9a97d-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a97d-141">System.String</span></span>

## <span data-ttu-id="9a97d-142">출력</span><span class="sxs-lookup"><span data-stu-id="9a97d-142">OUTPUTS</span></span>

### <span data-ttu-id="9a97d-143">NodeConfiguration를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="9a97d-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="9a97d-144">상속자</span><span class="sxs-lookup"><span data-stu-id="9a97d-144">NOTES</span></span>

## <span data-ttu-id="9a97d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a97d-145">RELATED LINKS</span></span>

[<span data-ttu-id="9a97d-146">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a97d-146">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="9a97d-147">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a97d-147">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)


