---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 44d22938d2d9fd8d7830acf676ac0b953c6bdc4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976987"
---
# <span data-ttu-id="71934-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="71934-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="71934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71934-102">SYNOPSIS</span></span>
<span data-ttu-id="71934-103">Azure 키 자격 증명 모음의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="71934-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="71934-104">구문</span><span class="sxs-lookup"><span data-stu-id="71934-104">SYNTAX</span></span>

### <span data-ttu-id="71934-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="71934-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71934-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71934-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71934-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71934-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71934-108">설명</span><span class="sxs-lookup"><span data-stu-id="71934-108">DESCRIPTION</span></span>
<span data-ttu-id="71934-109">이 cmdlet은 Azure 키 자격 증명 모음의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="71934-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="71934-110">예제</span><span class="sxs-lookup"><span data-stu-id="71934-110">EXAMPLES</span></span>

### <span data-ttu-id="71934-111">예제 1: 제거 보호 사용</span><span class="sxs-lookup"><span data-stu-id="71934-111">Example 1： Enable purge protection</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="71934-112">배관 구문을 사용하여 제거 보호를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71934-112">Enables purge protection using piping syntax.</span></span>

### <span data-ttu-id="71934-113">예제 2: RBAC 권한 부여 사용</span><span class="sxs-lookup"><span data-stu-id="71934-113">Example 2： Enable RBAC Authorization</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnableRbacAuthorization $true
```

<span data-ttu-id="71934-114">배관 구문을 사용하여 RBAC 권한 부여를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71934-114">Enables RBAC Authorization using piping syntax.</span></span>

### <span data-ttu-id="71934-115">예제 3: 태그 설정</span><span class="sxs-lookup"><span data-stu-id="71934-115">Example 3： Set tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{key = "value"}
```

<span data-ttu-id="71934-116">키 자격 증명 모음이라는 태그를 $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="71934-116">Sets the tags of a key vault named $keyVaultName.</span></span>

### <span data-ttu-id="71934-117">예제 4: 태그 정리</span><span class="sxs-lookup"><span data-stu-id="71934-117">Example 4： Clean tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{}
```

<span data-ttu-id="71934-118">키 자격 증명 모음이라는 키 자격 증명 모음의 모든 태그를 $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="71934-118">Deletes all tags of a key vault named $keyVaultName.</span></span>

## <span data-ttu-id="71934-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="71934-119">PARAMETERS</span></span>

### <span data-ttu-id="71934-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71934-120">-DefaultProfile</span></span>
<span data-ttu-id="71934-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71934-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71934-122">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="71934-122">-EnablePurgeProtection</span></span>
<span data-ttu-id="71934-123">이 키 자격 증명 모음에 대한 제거 보호 기능을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="71934-123">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="71934-124">일단 사용하도록 설정되면 사용하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="71934-124">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="71934-125">소프트 삭제를 켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="71934-125">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="71934-126">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="71934-126">-EnableRbacAuthorization</span></span>
<span data-ttu-id="71934-127">이 키 자격 증명 모음을 사용하도록 설정하거나 사용하지 않도록 설정하여 RBAC(역할 기반 액세스 제어)에 의해 데이터 작업을 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="71934-127">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71934-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71934-128">-InputObject</span></span>
<span data-ttu-id="71934-129">키 자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="71934-129">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71934-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71934-130">-ResourceGroupName</span></span>
<span data-ttu-id="71934-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71934-131">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71934-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71934-132">-ResourceId</span></span>
<span data-ttu-id="71934-133">키 자격 증명 모음의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="71934-133">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71934-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="71934-134">-Tag</span></span>
<span data-ttu-id="71934-135">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="71934-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71934-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="71934-136">-VaultName</span></span>
<span data-ttu-id="71934-137">키 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71934-137">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71934-138">-확인</span><span class="sxs-lookup"><span data-stu-id="71934-138">-Confirm</span></span>
<span data-ttu-id="71934-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71934-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71934-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71934-140">-WhatIf</span></span>
<span data-ttu-id="71934-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="71934-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71934-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71934-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71934-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71934-143">CommonParameters</span></span>
<span data-ttu-id="71934-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71934-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71934-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71934-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71934-146">입력</span><span class="sxs-lookup"><span data-stu-id="71934-146">INPUTS</span></span>

### <span data-ttu-id="71934-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="71934-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="71934-148">System.String</span><span class="sxs-lookup"><span data-stu-id="71934-148">System.String</span></span>

## <span data-ttu-id="71934-149">출력</span><span class="sxs-lookup"><span data-stu-id="71934-149">OUTPUTS</span></span>

### <span data-ttu-id="71934-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="71934-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="71934-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71934-151">NOTES</span></span>

## <span data-ttu-id="71934-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71934-152">RELATED LINKS</span></span>
