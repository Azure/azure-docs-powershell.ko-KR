---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 2a9c2870e0ce33b93d3013e84e7de3642b42708c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334970"
---
# <span data-ttu-id="154c0-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="154c0-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="154c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="154c0-102">SYNOPSIS</span></span>
<span data-ttu-id="154c0-103">Azure Key Vault의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="154c0-104">구문</span><span class="sxs-lookup"><span data-stu-id="154c0-104">SYNTAX</span></span>

### <span data-ttu-id="154c0-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="154c0-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="154c0-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="154c0-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="154c0-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="154c0-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="154c0-108">설명</span><span class="sxs-lookup"><span data-stu-id="154c0-108">DESCRIPTION</span></span>
<span data-ttu-id="154c0-109">이 cmdlet은 Azure Key Vault의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="154c0-110">예제</span><span class="sxs-lookup"><span data-stu-id="154c0-110">EXAMPLES</span></span>

### <span data-ttu-id="154c0-111">예제 1: 제거 보호 사용</span><span class="sxs-lookup"><span data-stu-id="154c0-111">Example 1： Enable purge protection</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="154c0-112">파이핑 구문을 사용하여 제거 보호를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-112">Enables purge protection using piping syntax.</span></span>

### <span data-ttu-id="154c0-113">예제 2: RBAC 권한 부여 사용</span><span class="sxs-lookup"><span data-stu-id="154c0-113">Example 2： Enable RBAC Authorization</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnableRbacAuthorization $true
```

<span data-ttu-id="154c0-114">파이핑 구문을 사용하여 RBAC 권한 부여를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-114">Enables RBAC Authorization using piping syntax.</span></span>

### <span data-ttu-id="154c0-115">예제 3: 태그 설정</span><span class="sxs-lookup"><span data-stu-id="154c0-115">Example 3： Set tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{key = "value"}
```

<span data-ttu-id="154c0-116">자격 증명 모음이라는 키 자격 증명 모음의 태그를 $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="154c0-116">Sets the tags of a key vault named $keyVaultName.</span></span>

### <span data-ttu-id="154c0-117">예제 4: 태그 정리</span><span class="sxs-lookup"><span data-stu-id="154c0-117">Example 4： Clean tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{}
```

<span data-ttu-id="154c0-118">자격 증명 모음이라는 키 자격 증명 모음의 모든 태그를 $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="154c0-118">Deletes all tags of a key vault named $keyVaultName.</span></span>

## <span data-ttu-id="154c0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="154c0-119">PARAMETERS</span></span>

### <span data-ttu-id="154c0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154c0-120">-DefaultProfile</span></span>
<span data-ttu-id="154c0-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="154c0-122">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="154c0-122">-EnablePurgeProtection</span></span>
<span data-ttu-id="154c0-123">이 키 자격 증명 모음에 대한 제거 보호 기능을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="154c0-123">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="154c0-124">사용하도록 설정하면 비활성화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-124">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="154c0-125">소프트 삭제를 켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-125">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="154c0-126">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="154c0-126">-EnableRbacAuthorization</span></span>
<span data-ttu-id="154c0-127">RBAC(역할 기반 Access Control)에서 데이터 작업에 권한을 부여하려면 이 키 자격 증명 모음을 사용하도록 설정하거나 사용하지 않도록 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="154c0-127">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="154c0-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="154c0-128">-InputObject</span></span>
<span data-ttu-id="154c0-129">Key Vault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-129">Key vault object.</span></span>

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

### <span data-ttu-id="154c0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="154c0-130">-ResourceGroupName</span></span>
<span data-ttu-id="154c0-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="154c0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="154c0-132">-ResourceId</span></span>
<span data-ttu-id="154c0-133">키 자격 증명 모음의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-133">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="154c0-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="154c0-134">-Tag</span></span>
<span data-ttu-id="154c0-135">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-135">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="154c0-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="154c0-136">-VaultName</span></span>
<span data-ttu-id="154c0-137">키 자격 증명 모음의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-137">Name of the key vault.</span></span>

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

### <span data-ttu-id="154c0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="154c0-138">-Confirm</span></span>
<span data-ttu-id="154c0-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="154c0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="154c0-140">-WhatIf</span></span>
<span data-ttu-id="154c0-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="154c0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="154c0-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="154c0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154c0-143">CommonParameters</span></span>
<span data-ttu-id="154c0-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="154c0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154c0-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="154c0-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154c0-146">입력</span><span class="sxs-lookup"><span data-stu-id="154c0-146">INPUTS</span></span>

### <span data-ttu-id="154c0-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="154c0-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="154c0-148">System.String</span><span class="sxs-lookup"><span data-stu-id="154c0-148">System.String</span></span>

## <span data-ttu-id="154c0-149">출력</span><span class="sxs-lookup"><span data-stu-id="154c0-149">OUTPUTS</span></span>

### <span data-ttu-id="154c0-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="154c0-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="154c0-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="154c0-151">NOTES</span></span>

## <span data-ttu-id="154c0-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="154c0-152">RELATED LINKS</span></span>
