---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176820"
---
# <span data-ttu-id="82497-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="82497-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="82497-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82497-102">SYNOPSIS</span></span>
<span data-ttu-id="82497-103">관리되는 인스턴스에서 Key Vault SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="82497-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="82497-104">구문</span><span class="sxs-lookup"><span data-stu-id="82497-104">SYNTAX</span></span>

### <span data-ttu-id="82497-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="82497-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82497-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82497-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82497-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82497-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82497-108">설명</span><span class="sxs-lookup"><span data-stu-id="82497-108">DESCRIPTION</span></span>
<span data-ttu-id="82497-109">이 Remove-AzSqlInstanceKeyVaultKey cmdlet은 지정된 Managed Instance에서 Key Vault 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="82497-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="82497-110">키의 SQL 관리되는 인스턴스의 사용 권한은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82497-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="82497-111">사용 권한을 변경하려면 Set-AzKeyVaultAccessPolicy를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="82497-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="82497-112">이 cmdlet은 Key Vault를 변경하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82497-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="82497-113">Key Vault에서 키를 제거하려면 Remove-AzureKeyVaultKey를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="82497-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="82497-114">예제</span><span class="sxs-lookup"><span data-stu-id="82497-114">EXAMPLES</span></span>

### <span data-ttu-id="82497-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="82497-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="82497-116">이 명령은 지정된 관리되는 인스턴스에서 ID '를 사용하여 Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="82497-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="82497-117">예제 2: 관리되는 인스턴스 개체 사용</span><span class="sxs-lookup"><span data-stu-id="82497-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="82497-118">이 명령은 지정된 관리되는 인스턴스에서 ID '를 사용하여 Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="82497-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="82497-119">예제 3: 관리되는 인스턴스 리소스 ID 사용</span><span class="sxs-lookup"><span data-stu-id="82497-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="82497-120">이 명령은 지정된 관리되는 인스턴스에서 ID '를 사용하여 Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="82497-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="82497-121">예제 4: 파이핑 사용</span><span class="sxs-lookup"><span data-stu-id="82497-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="82497-122">이 명령은 지정된 관리되는 인스턴스에서 ID '를 사용하여 Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="82497-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="82497-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82497-123">PARAMETERS</span></span>

### <span data-ttu-id="82497-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82497-124">-DefaultProfile</span></span>
<span data-ttu-id="82497-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82497-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82497-126">-Instance</span><span class="sxs-lookup"><span data-stu-id="82497-126">-Instance</span></span>
<span data-ttu-id="82497-127">인스턴스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="82497-127">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82497-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="82497-128">-InstanceName</span></span>
<span data-ttu-id="82497-129">인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="82497-129">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82497-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="82497-130">-InstanceResourceId</span></span>
<span data-ttu-id="82497-131">인스턴스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="82497-131">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82497-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="82497-132">-KeyId</span></span>
<span data-ttu-id="82497-133">AzureKeyVault 키 ID</span><span class="sxs-lookup"><span data-stu-id="82497-133">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82497-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82497-134">-ResourceGroupName</span></span>
<span data-ttu-id="82497-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="82497-135">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82497-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82497-136">-Confirm</span></span>
<span data-ttu-id="82497-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82497-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82497-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82497-138">-WhatIf</span></span>
<span data-ttu-id="82497-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="82497-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82497-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82497-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82497-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82497-141">CommonParameters</span></span>
<span data-ttu-id="82497-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82497-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82497-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82497-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82497-144">입력</span><span class="sxs-lookup"><span data-stu-id="82497-144">INPUTS</span></span>

### <span data-ttu-id="82497-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="82497-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="82497-146">System.String</span><span class="sxs-lookup"><span data-stu-id="82497-146">System.String</span></span>

## <span data-ttu-id="82497-147">출력</span><span class="sxs-lookup"><span data-stu-id="82497-147">OUTPUTS</span></span>

### <span data-ttu-id="82497-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="82497-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="82497-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82497-149">NOTES</span></span>

## <span data-ttu-id="82497-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82497-150">RELATED LINKS</span></span>
