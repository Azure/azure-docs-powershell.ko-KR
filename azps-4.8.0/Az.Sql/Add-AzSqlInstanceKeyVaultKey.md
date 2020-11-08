---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048718"
---
# <span data-ttu-id="f3577-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f3577-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="f3577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3577-102">SYNOPSIS</span></span>
<span data-ttu-id="f3577-103">제공 된 관리 되는 인스턴스에 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="f3577-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3577-104">SYNTAX</span></span>

### <span data-ttu-id="f3577-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3577-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3577-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3577-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3577-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3577-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3577-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f3577-108">DESCRIPTION</span></span>
<span data-ttu-id="f3577-109">Add-AzSqlInstanceKeyVaultKey cmdlet은 제공 된 관리 인스턴스에 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="f3577-110">관리 되는 인스턴스에는 자격 증명 모음에 대 한 ' get, wrapKey, unwrapKey ' 사용 권한이 있어야 하며, 다음 스크립트를 사용 하 여 관리 되는 인스턴스에 대 한 사용 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="f3577-111">$managedInstance = Get-AzSqlInstance-Name ' ContosoManagedInstanceName '-ResourceGroupName ' ContosoResourceGroup ' Set-AzKeyVaultAccessPolicy-VaultName ContosoVault-ObjectId $managedInstance. Id. PrincipalId-Stokeys get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="f3577-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="f3577-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f3577-112">EXAMPLES</span></span>

### <span data-ttu-id="f3577-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3577-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f3577-114">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 리소스 그룹 ' ContosoResourceGroup '에서 이름이 ' ContosoManagedInstanceName ' 인 SQL 관리 인스턴스에 Id가 ' ' 인 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="f3577-115">예제 2: 관리 되는 인스턴스 개체 사용</span><span class="sxs-lookup"><span data-stu-id="f3577-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f3577-116">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 리소스 그룹 ' ContosoResourceGroup '에서 이름이 ' ContosoManagedInstanceName ' 인 SQL 관리 인스턴스에 Id가 ' ' 인 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="f3577-117">예제 3: 관리 되는 인스턴스 리소스 id 사용</span><span class="sxs-lookup"><span data-stu-id="f3577-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f3577-118">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 리소스 그룹 ' ContosoResourceGroup '에서 이름이 ' ContosoManagedInstanceName ' 인 SQL 관리 인스턴스에 Id가 ' ' 인 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="f3577-119">예제 4: 배관 사용</span><span class="sxs-lookup"><span data-stu-id="f3577-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f3577-120">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 리소스 그룹 ' ContosoResourceGroup '에서 이름이 ' ContosoManagedInstanceName ' 인 SQL 관리 인스턴스에 Id가 ' ' 인 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="f3577-121">변수</span><span class="sxs-lookup"><span data-stu-id="f3577-121">PARAMETERS</span></span>

### <span data-ttu-id="f3577-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3577-122">-DefaultProfile</span></span>
<span data-ttu-id="f3577-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3577-124">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="f3577-124">-Instance</span></span>
<span data-ttu-id="f3577-125">인스턴스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="f3577-125">The instance input object</span></span>

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

### <span data-ttu-id="f3577-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f3577-126">-InstanceName</span></span>
<span data-ttu-id="f3577-127">인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="f3577-127">The instance name</span></span>

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

### <span data-ttu-id="f3577-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="f3577-128">-InstanceResourceId</span></span>
<span data-ttu-id="f3577-129">인스턴스 리소스 id</span><span class="sxs-lookup"><span data-stu-id="f3577-129">The instance resource id</span></span>

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

### <span data-ttu-id="f3577-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f3577-130">-KeyId</span></span>
<span data-ttu-id="f3577-131">AzureKeyVault 키 id</span><span class="sxs-lookup"><span data-stu-id="f3577-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="f3577-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3577-132">-ResourceGroupName</span></span>
<span data-ttu-id="f3577-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f3577-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="f3577-134">-확인</span><span class="sxs-lookup"><span data-stu-id="f3577-134">-Confirm</span></span>
<span data-ttu-id="f3577-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3577-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3577-136">-WhatIf</span></span>
<span data-ttu-id="f3577-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3577-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3577-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3577-139">CommonParameters</span></span>
<span data-ttu-id="f3577-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3577-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3577-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f3577-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3577-142">입력</span><span class="sxs-lookup"><span data-stu-id="f3577-142">INPUTS</span></span>

### <span data-ttu-id="f3577-143">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="f3577-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="f3577-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3577-144">System.String</span></span>

## <span data-ttu-id="f3577-145">출력</span><span class="sxs-lookup"><span data-stu-id="f3577-145">OUTPUTS</span></span>

### <span data-ttu-id="f3577-146">TransparentDataEncryption. AzureRmSqlManagedInstanceKeyVaultKeyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="f3577-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="f3577-147">상속자</span><span class="sxs-lookup"><span data-stu-id="f3577-147">NOTES</span></span>

## <span data-ttu-id="f3577-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3577-148">RELATED LINKS</span></span>
