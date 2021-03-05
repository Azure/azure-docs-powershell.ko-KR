---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: a52d1d44647d2b608a34a07722439f243ba08510
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008832"
---
# <span data-ttu-id="8357b-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8357b-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="8357b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8357b-102">SYNOPSIS</span></span>
<span data-ttu-id="8357b-103">통합 계정 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="8357b-104">구문</span><span class="sxs-lookup"><span data-stu-id="8357b-104">SYNTAX</span></span>

### <span data-ttu-id="8357b-105">ByIntegrationAccountAndFilePath(기본값)</span><span class="sxs-lookup"><span data-stu-id="8357b-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8357b-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="8357b-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8357b-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="8357b-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8357b-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="8357b-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8357b-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="8357b-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8357b-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="8357b-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8357b-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="8357b-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8357b-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="8357b-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8357b-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="8357b-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8357b-114">설명</span><span class="sxs-lookup"><span data-stu-id="8357b-114">DESCRIPTION</span></span>
<span data-ttu-id="8357b-115">**Get-AzIntegrationAccountAssembly** cmdlet은 통합 계정에 새 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="8357b-116">예제</span><span class="sxs-lookup"><span data-stu-id="8357b-116">EXAMPLES</span></span>

### <span data-ttu-id="8357b-117">예제 1: 로컬 파일을 사용하여 새 어셈블리 만들기</span><span class="sxs-lookup"><span data-stu-id="8357b-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="8357b-118">"$localAssemblyFilePath"에 포함된 파일 경로에 있는 로컬 파일을 사용하여 새 어셈블리를 $localAssemblyFilePath.</span><span class="sxs-lookup"><span data-stu-id="8357b-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="8357b-119">예제 2: byte 데이터를 사용하여 새 어셈블리 만들기</span><span class="sxs-lookup"><span data-stu-id="8357b-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="8357b-120">"$assemblyContent"에 포함된 $assemblyContent.</span><span class="sxs-lookup"><span data-stu-id="8357b-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="8357b-121">예제 3: 콘텐츠 링크를 사용하여 새 어셈블리 만들기</span><span class="sxs-lookup"><span data-stu-id="8357b-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="8357b-122">"$assemblyUrl"에 있는 byte 데이터를 사용하여 새 어셈블리를 $assemblyUrl.</span><span class="sxs-lookup"><span data-stu-id="8357b-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="8357b-123">크기가 큰 어셈블리를 만드는 데 제안된 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="8357b-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8357b-124">PARAMETERS</span></span>

### <span data-ttu-id="8357b-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="8357b-125">-AssemblyData</span></span>
<span data-ttu-id="8357b-126">통합 계정 어셈블리 byte 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="8357b-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="8357b-127">-AssemblyFilePath</span></span>
<span data-ttu-id="8357b-128">통합 계정 어셈블리 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="8357b-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="8357b-129">-ContentLink</span></span>
<span data-ttu-id="8357b-130">통합 계정 어셈블리 데이터에 대한 공개적으로 액세스할 수 있는 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="8357b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8357b-131">-DefaultProfile</span></span>
<span data-ttu-id="8357b-132">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8357b-133">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="8357b-133">-Metadata</span></span>
<span data-ttu-id="8357b-134">통합 계정 어셈블리 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="8357b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="8357b-135">-Name</span></span>
<span data-ttu-id="8357b-136">통합 계정 어셈블리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="8357b-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="8357b-137">-ParentName</span></span>
<span data-ttu-id="8357b-138">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-138">The integration account name.</span></span>

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

### <span data-ttu-id="8357b-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8357b-139">-ParentObject</span></span>
<span data-ttu-id="8357b-140">통합 계정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-140">An integration account object.</span></span>

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

### <span data-ttu-id="8357b-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8357b-141">-ParentResourceId</span></span>
<span data-ttu-id="8357b-142">통합 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="8357b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8357b-143">-ResourceGroupName</span></span>
<span data-ttu-id="8357b-144">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-144">The resource group name.</span></span>

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

### <span data-ttu-id="8357b-145">-확인</span><span class="sxs-lookup"><span data-stu-id="8357b-145">-Confirm</span></span>
<span data-ttu-id="8357b-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8357b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8357b-147">-WhatIf</span></span>
<span data-ttu-id="8357b-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8357b-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8357b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8357b-150">CommonParameters</span></span>
<span data-ttu-id="8357b-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8357b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8357b-152">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8357b-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8357b-153">입력</span><span class="sxs-lookup"><span data-stu-id="8357b-153">INPUTS</span></span>

### <span data-ttu-id="8357b-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8357b-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="8357b-155">System.String</span><span class="sxs-lookup"><span data-stu-id="8357b-155">System.String</span></span>

## <span data-ttu-id="8357b-156">출력</span><span class="sxs-lookup"><span data-stu-id="8357b-156">OUTPUTS</span></span>

### <span data-ttu-id="8357b-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8357b-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="8357b-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8357b-158">NOTES</span></span>

## <span data-ttu-id="8357b-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8357b-159">RELATED LINKS</span></span>
