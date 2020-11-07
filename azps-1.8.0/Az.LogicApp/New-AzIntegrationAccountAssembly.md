---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 41f2e9c99c219ce34eee8ad4a0fde9b63616b7f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867694"
---
# <span data-ttu-id="ce153-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ce153-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="ce153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce153-102">SYNOPSIS</span></span>
<span data-ttu-id="ce153-103">통합 계정 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="ce153-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce153-104">SYNTAX</span></span>

### <span data-ttu-id="ce153-105">ByIntegrationAccountAndFilePath (기본값)</span><span class="sxs-lookup"><span data-stu-id="ce153-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce153-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="ce153-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce153-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="ce153-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce153-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="ce153-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce153-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="ce153-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce153-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="ce153-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce153-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="ce153-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce153-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="ce153-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce153-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="ce153-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce153-114">설명은</span><span class="sxs-lookup"><span data-stu-id="ce153-114">DESCRIPTION</span></span>
<span data-ttu-id="ce153-115">**Get-AzIntegrationAccountAssembly** cmdlet은 통합 계정에 새 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="ce153-116">예제의</span><span class="sxs-lookup"><span data-stu-id="ce153-116">EXAMPLES</span></span>

### <span data-ttu-id="ce153-117">예제 1: 로컬 파일을 사용 하 여 새 어셈블리 만들기</span><span class="sxs-lookup"><span data-stu-id="ce153-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="ce153-118">"$LocalAssemblyFilePath"에 포함 된 파일 경로에 있는 로컬 파일을 사용 하 여 새 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="ce153-119">예제 2: 바이트 데이터를 사용 하 여 새 어셈블리 만들기</span><span class="sxs-lookup"><span data-stu-id="ce153-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="ce153-120">"$AssemblyContent"에 포함 된 a 바이트 배열을 사용 하 여 새 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="ce153-121">예제 3: 콘텐츠 링크를 사용 하 여 새 어셈블리 만들기</span><span class="sxs-lookup"><span data-stu-id="ce153-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="ce153-122">URL "$assemblyUrl"에 있는 a 바이트 데이터를 사용 하 여 새 어셈블리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="ce153-123">이 방법은 크기가 큰 어셈블리를 만들 때 제안 되는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="ce153-124">변수</span><span class="sxs-lookup"><span data-stu-id="ce153-124">PARAMETERS</span></span>

### <span data-ttu-id="ce153-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="ce153-125">-AssemblyData</span></span>
<span data-ttu-id="ce153-126">통합 계정 어셈블리 바이트 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="ce153-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="ce153-127">-AssemblyFilePath</span></span>
<span data-ttu-id="ce153-128">통합 계정 어셈블리 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="ce153-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="ce153-129">-ContentLink</span></span>
<span data-ttu-id="ce153-130">통합 계정 어셈블리 데이터에 대 한 공개적으로 액세스할 수 있는 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="ce153-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce153-131">-DefaultProfile</span></span>
<span data-ttu-id="ce153-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce153-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ce153-133">-Metadata</span></span>
<span data-ttu-id="ce153-134">통합 계정 어셈블리 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="ce153-135">-이름</span><span class="sxs-lookup"><span data-stu-id="ce153-135">-Name</span></span>
<span data-ttu-id="ce153-136">통합 계정 어셈블리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="ce153-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="ce153-137">-ParentName</span></span>
<span data-ttu-id="ce153-138">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-138">The integration account name.</span></span>

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

### <span data-ttu-id="ce153-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ce153-139">-ParentObject</span></span>
<span data-ttu-id="ce153-140">통합 계정 개체</span><span class="sxs-lookup"><span data-stu-id="ce153-140">An integration account object.</span></span>

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

### <span data-ttu-id="ce153-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ce153-141">-ParentResourceId</span></span>
<span data-ttu-id="ce153-142">통합 계정 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="ce153-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce153-143">-ResourceGroupName</span></span>
<span data-ttu-id="ce153-144">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-144">The resource group name.</span></span>

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

### <span data-ttu-id="ce153-145">-확인</span><span class="sxs-lookup"><span data-stu-id="ce153-145">-Confirm</span></span>
<span data-ttu-id="ce153-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce153-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce153-147">-WhatIf</span></span>
<span data-ttu-id="ce153-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce153-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce153-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce153-150">CommonParameters</span></span>
<span data-ttu-id="ce153-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce153-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce153-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce153-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce153-153">입력</span><span class="sxs-lookup"><span data-stu-id="ce153-153">INPUTS</span></span>

### <span data-ttu-id="ce153-154">IntegrationAccount를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="ce153-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="ce153-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ce153-155">System.String</span></span>

## <span data-ttu-id="ce153-156">출력</span><span class="sxs-lookup"><span data-stu-id="ce153-156">OUTPUTS</span></span>

### <span data-ttu-id="ce153-157">LogicApp. PSIntegrationAccountAssembly/.</span><span class="sxs-lookup"><span data-stu-id="ce153-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="ce153-158">상속자</span><span class="sxs-lookup"><span data-stu-id="ce153-158">NOTES</span></span>

## <span data-ttu-id="ce153-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce153-159">RELATED LINKS</span></span>
