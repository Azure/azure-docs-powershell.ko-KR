---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489384"
---
# <span data-ttu-id="5b0c6-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5b0c6-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="5b0c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0c6-103">통합 계정 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="5b0c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b0c6-104">SYNTAX</span></span>

### <span data-ttu-id="5b0c6-105">ByIntegrationAccountAndFilePath(기본값)</span><span class="sxs-lookup"><span data-stu-id="5b0c6-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0c6-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5b0c6-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b0c6-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5b0c6-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b0c6-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5b0c6-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0c6-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5b0c6-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0c6-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="5b0c6-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0c6-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5b0c6-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0c6-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5b0c6-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0c6-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="5b0c6-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b0c6-114">설명</span><span class="sxs-lookup"><span data-stu-id="5b0c6-114">DESCRIPTION</span></span>
<span data-ttu-id="5b0c6-115">**Get-AzIntegrationAccountAssembly** cmdlet은 통합 계정에 새 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="5b0c6-116">예제</span><span class="sxs-lookup"><span data-stu-id="5b0c6-116">EXAMPLES</span></span>

### <span data-ttu-id="5b0c6-117">예제 1: 로컬 파일을 사용하여 새 어셈블리 만들기</span><span class="sxs-lookup"><span data-stu-id="5b0c6-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5b0c6-118">"$localAssemblyFilePath"에 포함된 파일 경로에 있는 로컬 파일을 사용하여 새 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="5b0c6-119">예제 2: Byte 데이터를 사용하여 새 어셈블리 만들기</span><span class="sxs-lookup"><span data-stu-id="5b0c6-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5b0c6-120">"$assemblyContent"에 포함된 byte 배열을 사용하여 새 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="5b0c6-121">예제 3: 콘텐츠 링크를 사용하여 새 어셈블리 만들기</span><span class="sxs-lookup"><span data-stu-id="5b0c6-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5b0c6-122">URL "$assemblyUrl"에 있는 byte 데이터를 사용하여 새 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="5b0c6-123">이는 큰 크기의 어셈블리를 만들기 위한 제안된 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="5b0c6-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b0c6-124">PARAMETERS</span></span>

### <span data-ttu-id="5b0c6-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="5b0c6-125">-AssemblyData</span></span>
<span data-ttu-id="5b0c6-126">통합 계정 어셈블리 byte 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="5b0c6-127">-AssemblyFilePath</span></span>
<span data-ttu-id="5b0c6-128">통합 계정 어셈블리 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="5b0c6-129">-ContentLink</span></span>
<span data-ttu-id="5b0c6-130">통합 계정 어셈블리 데이터에 대한 공개적으로 액세스할 수 있는 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b0c6-131">-DefaultProfile</span></span>
<span data-ttu-id="5b0c6-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b0c6-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5b0c6-133">-Metadata</span></span>
<span data-ttu-id="5b0c6-134">통합 계정 어셈블리 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-134">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-135">-Name</span><span class="sxs-lookup"><span data-stu-id="5b0c6-135">-Name</span></span>
<span data-ttu-id="5b0c6-136">통합 계정 어셈블리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="5b0c6-137">-ParentName</span></span>
<span data-ttu-id="5b0c6-138">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-138">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5b0c6-139">-ParentObject</span></span>
<span data-ttu-id="5b0c6-140">통합 계정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5b0c6-141">-ParentResourceId</span></span>
<span data-ttu-id="5b0c6-142">통합 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-142">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b0c6-143">-ResourceGroupName</span></span>
<span data-ttu-id="5b0c6-144">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-144">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b0c6-145">-Confirm</span></span>
<span data-ttu-id="5b0c6-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b0c6-147">-WhatIf</span></span>
<span data-ttu-id="5b0c6-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5b0c6-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b0c6-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0c6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0c6-150">CommonParameters</span></span>
<span data-ttu-id="5b0c6-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0c6-152">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b0c6-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0c6-153">입력</span><span class="sxs-lookup"><span data-stu-id="5b0c6-153">INPUTS</span></span>

### <span data-ttu-id="5b0c6-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5b0c6-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="5b0c6-155">System.String</span><span class="sxs-lookup"><span data-stu-id="5b0c6-155">System.String</span></span>

## <span data-ttu-id="5b0c6-156">출력</span><span class="sxs-lookup"><span data-stu-id="5b0c6-156">OUTPUTS</span></span>

### <span data-ttu-id="5b0c6-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5b0c6-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="5b0c6-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b0c6-158">NOTES</span></span>

## <span data-ttu-id="5b0c6-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b0c6-159">RELATED LINKS</span></span>
