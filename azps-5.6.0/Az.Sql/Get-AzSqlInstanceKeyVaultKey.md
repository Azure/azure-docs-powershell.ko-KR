---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 05c9565152063f10fb80d04fab0264807e9f3308
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999355"
---
# <span data-ttu-id="ccf90-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ccf90-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="ccf90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccf90-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf90-103">관리되는 SQL Key Vault 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="ccf90-104">구문</span><span class="sxs-lookup"><span data-stu-id="ccf90-104">SYNTAX</span></span>

### <span data-ttu-id="ccf90-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ccf90-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf90-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccf90-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf90-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccf90-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccf90-108">설명</span><span class="sxs-lookup"><span data-stu-id="ccf90-108">DESCRIPTION</span></span>
<span data-ttu-id="ccf90-109">Get-AzSqlInstanceKeyVaultKey cmdlet은 관리되는 SQL Key Vault 키에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="ccf90-110">관리되는 인스턴스의 모든 키를 보거나 KeyId를 제공하여 특정 키를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="ccf90-111">예제</span><span class="sxs-lookup"><span data-stu-id="ccf90-111">EXAMPLES</span></span>

### <span data-ttu-id="ccf90-112">예제 1: 모든 Key Vault 키 사용</span><span class="sxs-lookup"><span data-stu-id="ccf90-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="ccf90-113">이 명령은 관리되는 인스턴스의 모든 Key Vault 키를 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="ccf90-114">예제 2: 특정 Key Vault 키 사용</span><span class="sxs-lookup"><span data-stu-id="ccf90-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="ccf90-115">이 명령은 Id ''를 사용하여 Key Vault 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="ccf90-116">예제 3: 인스턴스 개체 사용</span><span class="sxs-lookup"><span data-stu-id="ccf90-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="ccf90-117">이 명령은 Id ''를 사용하여 Key Vault 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="ccf90-118">예제 4: 인스턴스 리소스 ID 사용</span><span class="sxs-lookup"><span data-stu-id="ccf90-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="ccf90-119">이 명령은 Id ''를 사용하여 Key Vault 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="ccf90-120">예제 5: 배관 사용</span><span class="sxs-lookup"><span data-stu-id="ccf90-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="ccf90-121">이 명령은 Id ''를 사용하여 Key Vault 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="ccf90-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ccf90-122">PARAMETERS</span></span>

### <span data-ttu-id="ccf90-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf90-123">-DefaultProfile</span></span>
<span data-ttu-id="ccf90-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccf90-125">-Instance</span><span class="sxs-lookup"><span data-stu-id="ccf90-125">-Instance</span></span>
<span data-ttu-id="ccf90-126">인스턴스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="ccf90-126">The instance input object</span></span>

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

### <span data-ttu-id="ccf90-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ccf90-127">-InstanceName</span></span>
<span data-ttu-id="ccf90-128">인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="ccf90-128">The instance name</span></span>

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

### <span data-ttu-id="ccf90-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="ccf90-129">-InstanceResourceId</span></span>
<span data-ttu-id="ccf90-130">인스턴스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ccf90-130">The instance resource id</span></span>

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

### <span data-ttu-id="ccf90-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="ccf90-131">-KeyId</span></span>
<span data-ttu-id="ccf90-132">AzureKeyVault 키 ID</span><span class="sxs-lookup"><span data-stu-id="ccf90-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf90-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf90-133">-ResourceGroupName</span></span>
<span data-ttu-id="ccf90-134">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ccf90-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="ccf90-135">-확인</span><span class="sxs-lookup"><span data-stu-id="ccf90-135">-Confirm</span></span>
<span data-ttu-id="ccf90-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccf90-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf90-137">-WhatIf</span></span>
<span data-ttu-id="ccf90-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccf90-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccf90-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf90-140">CommonParameters</span></span>
<span data-ttu-id="ccf90-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf90-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf90-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccf90-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf90-143">입력</span><span class="sxs-lookup"><span data-stu-id="ccf90-143">INPUTS</span></span>

### <span data-ttu-id="ccf90-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ccf90-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="ccf90-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ccf90-145">System.String</span></span>

## <span data-ttu-id="ccf90-146">출력</span><span class="sxs-lookup"><span data-stu-id="ccf90-146">OUTPUTS</span></span>

### <span data-ttu-id="ccf90-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="ccf90-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="ccf90-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ccf90-148">NOTES</span></span>

## <span data-ttu-id="ccf90-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccf90-149">RELATED LINKS</span></span>
