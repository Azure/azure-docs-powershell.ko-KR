---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343833"
---
# <span data-ttu-id="bffcf-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bffcf-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="bffcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bffcf-102">SYNOPSIS</span></span>
<span data-ttu-id="bffcf-103">통합 계정 어셈블리를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="bffcf-104">구문</span><span class="sxs-lookup"><span data-stu-id="bffcf-104">SYNTAX</span></span>

### <span data-ttu-id="bffcf-105">ByIntegrationAccountAndFilePath(기본값)</span><span class="sxs-lookup"><span data-stu-id="bffcf-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bffcf-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="bffcf-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bffcf-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="bffcf-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bffcf-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="bffcf-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bffcf-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="bffcf-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bffcf-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="bffcf-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bffcf-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="bffcf-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bffcf-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="bffcf-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bffcf-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="bffcf-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bffcf-114">설명</span><span class="sxs-lookup"><span data-stu-id="bffcf-114">DESCRIPTION</span></span>
<span data-ttu-id="bffcf-115">**Set-AzIntegrationAccountAssembly** cmdlet은 통합 계정 어셈블리를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="bffcf-116">예제</span><span class="sxs-lookup"><span data-stu-id="bffcf-116">EXAMPLES</span></span>

### <span data-ttu-id="bffcf-117">예제 1: 로컬 파일을 사용하여 어셈블리 수정</span><span class="sxs-lookup"><span data-stu-id="bffcf-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="bffcf-118">"$localAssemblyFilePath"에 포함된 파일 경로에 있는 로컬 파일을 사용하여 "sampleAssembly"라는 어셈블리를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="bffcf-119">예제 2: Byte 데이터를 사용하여 어셈블리 수정</span><span class="sxs-lookup"><span data-stu-id="bffcf-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="bffcf-120">"$assemblyContent"에 포함된 byte 배열을 사용하여 "sampleAssembly"라는 어셈블리를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="bffcf-121">예제 3: 콘텐츠 링크를 사용하여 어셈블리 수정</span><span class="sxs-lookup"><span data-stu-id="bffcf-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="bffcf-122">URL "$assemblyUrl"에 있는 byte 데이터를 사용하여 "sampleAssembly"라는 어셈블리를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="bffcf-123">이는 큰 크기의 어셈블리를 만들기 위한 제안된 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="bffcf-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bffcf-124">PARAMETERS</span></span>

### <span data-ttu-id="bffcf-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="bffcf-125">-AssemblyData</span></span>
<span data-ttu-id="bffcf-126">통합 계정 어셈블리 byte 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="bffcf-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="bffcf-127">-AssemblyFilePath</span></span>
<span data-ttu-id="bffcf-128">통합 계정 어셈블리 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="bffcf-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="bffcf-129">-ContentLink</span></span>
<span data-ttu-id="bffcf-130">통합 계정 어셈블리 데이터에 대한 공개적으로 액세스할 수 있는 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="bffcf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bffcf-131">-DefaultProfile</span></span>
<span data-ttu-id="bffcf-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bffcf-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bffcf-133">-InputObject</span></span>
<span data-ttu-id="bffcf-134">통합 계정 어셈블리입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bffcf-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="bffcf-135">-Metadata</span></span>
<span data-ttu-id="bffcf-136">통합 계정 어셈블리 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="bffcf-137">-Name</span><span class="sxs-lookup"><span data-stu-id="bffcf-137">-Name</span></span>
<span data-ttu-id="bffcf-138">통합 계정 어셈블리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffcf-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="bffcf-139">-ParentName</span></span>
<span data-ttu-id="bffcf-140">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-140">The integration account name.</span></span>

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

### <span data-ttu-id="bffcf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bffcf-141">-ResourceGroupName</span></span>
<span data-ttu-id="bffcf-142">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-142">The resource group name.</span></span>

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

### <span data-ttu-id="bffcf-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bffcf-143">-ResourceId</span></span>
<span data-ttu-id="bffcf-144">통합 계정 어셈블리 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="bffcf-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bffcf-145">-Confirm</span></span>
<span data-ttu-id="bffcf-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bffcf-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bffcf-147">-WhatIf</span></span>
<span data-ttu-id="bffcf-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bffcf-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bffcf-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bffcf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bffcf-150">CommonParameters</span></span>
<span data-ttu-id="bffcf-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bffcf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bffcf-152">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bffcf-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bffcf-153">입력</span><span class="sxs-lookup"><span data-stu-id="bffcf-153">INPUTS</span></span>

### <span data-ttu-id="bffcf-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bffcf-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="bffcf-155">System.String</span><span class="sxs-lookup"><span data-stu-id="bffcf-155">System.String</span></span>

## <span data-ttu-id="bffcf-156">출력</span><span class="sxs-lookup"><span data-stu-id="bffcf-156">OUTPUTS</span></span>

### <span data-ttu-id="bffcf-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bffcf-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="bffcf-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bffcf-158">NOTES</span></span>

## <span data-ttu-id="bffcf-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bffcf-159">RELATED LINKS</span></span>
