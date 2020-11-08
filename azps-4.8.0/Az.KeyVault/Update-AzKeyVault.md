---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 4302f2f9c4c2d6b2c7afa879fc28e2ff4edbb592
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211701"
---
# <span data-ttu-id="ee523-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ee523-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="ee523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee523-102">SYNOPSIS</span></span>
<span data-ttu-id="ee523-103">Azure 키 보관소의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="ee523-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee523-104">SYNTAX</span></span>

### <span data-ttu-id="ee523-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ee523-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee523-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee523-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee523-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee523-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee523-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ee523-108">DESCRIPTION</span></span>
<span data-ttu-id="ee523-109">이 cmdlet은 Azure 키 자격 증명 모음의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="ee523-110">예를 들어, 소프트 삭제를 사용 하도록 설정 하면 일부 속성을 업데이트 하는 것은 취소할 수 없으며, 더 이상 비활성화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="ee523-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ee523-111">EXAMPLES</span></span>

### <span data-ttu-id="ee523-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee523-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="ee523-113">리소스 그룹에 명명 된 키 보관소에 대해 일시 삭제를 사용 하도록 설정 `$keyVaultName` `$resourceGroupName` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="ee523-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee523-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="ee523-115">파이핑 구문을 사용한 지우기 보호를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="ee523-116">변수</span><span class="sxs-lookup"><span data-stu-id="ee523-116">PARAMETERS</span></span>

### <span data-ttu-id="ee523-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee523-117">-DefaultProfile</span></span>
<span data-ttu-id="ee523-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee523-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="ee523-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="ee523-120">이 키 자격 증명 모음에 대 한 보호 제거 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="ee523-121">활성화 한 후에는 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="ee523-122">이 기능을 사용 하려면 소프트 삭제가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-122">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="ee523-123">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee523-123">-EnableRbacAuthorization</span></span>
<span data-ttu-id="ee523-124">이 키 보관소를 사용 하거나 사용 하지 않도록 설정 하 여 역할별 (역할 기반 액세스 제어)로 데이터 작업을 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-124">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="ee523-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="ee523-125">-EnableSoftDelete</span></span>
<span data-ttu-id="ee523-126">이 키 자격 증명 모음에 대 한 소프트 삭제 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-126">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="ee523-127">활성화 한 후에는 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-127">Once enabled it cannot be disabled.</span></span>

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

### <span data-ttu-id="ee523-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee523-128">-InputObject</span></span>
<span data-ttu-id="ee523-129">키 자격 증명 모음 개체</span><span class="sxs-lookup"><span data-stu-id="ee523-129">Key vault object.</span></span>

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

### <span data-ttu-id="ee523-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee523-130">-ResourceGroupName</span></span>
<span data-ttu-id="ee523-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="ee523-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee523-132">-ResourceId</span></span>
<span data-ttu-id="ee523-133">키 자격 증명 모음의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-133">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="ee523-134">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ee523-134">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="ee523-135">삭제 된 리소스의 보존 기간 및 삭제 됨 상태의 개체를 제거할 수 있을 때까지 걸리는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-135">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="ee523-136">기본값은 90 일입니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-136">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee523-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ee523-137">-VaultName</span></span>
<span data-ttu-id="ee523-138">키 보관소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-138">Name of the key vault.</span></span>

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

### <span data-ttu-id="ee523-139">-확인</span><span class="sxs-lookup"><span data-stu-id="ee523-139">-Confirm</span></span>
<span data-ttu-id="ee523-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee523-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee523-141">-WhatIf</span></span>
<span data-ttu-id="ee523-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee523-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee523-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee523-144">CommonParameters</span></span>
<span data-ttu-id="ee523-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee523-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee523-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ee523-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee523-147">입력</span><span class="sxs-lookup"><span data-stu-id="ee523-147">INPUTS</span></span>

### <span data-ttu-id="ee523-148">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ee523-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ee523-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee523-149">System.String</span></span>

## <span data-ttu-id="ee523-150">출력</span><span class="sxs-lookup"><span data-stu-id="ee523-150">OUTPUTS</span></span>

### <span data-ttu-id="ee523-151">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ee523-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ee523-152">상속자</span><span class="sxs-lookup"><span data-stu-id="ee523-152">NOTES</span></span>

## <span data-ttu-id="ee523-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee523-153">RELATED LINKS</span></span>
