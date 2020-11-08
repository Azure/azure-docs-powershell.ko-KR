---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 61672d71c2b65ff3588f4a4d8827220695c2d8de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226083"
---
# <span data-ttu-id="53075-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="53075-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="53075-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53075-102">SYNOPSIS</span></span>
<span data-ttu-id="53075-103">SQL 관리 되는 인스턴스의 키 보관소 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53075-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="53075-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53075-104">SYNTAX</span></span>

### <span data-ttu-id="53075-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="53075-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53075-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53075-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53075-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53075-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53075-108">설명은</span><span class="sxs-lookup"><span data-stu-id="53075-108">DESCRIPTION</span></span>
<span data-ttu-id="53075-109">Get-AzSqlInstanceKeyVaultKey cmdlet은 SQL 관리 인스턴스의 키 자격 증명 키에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53075-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="53075-110">관리 되는 인스턴스의 모든 키를 보거나 KeyId을 제공 하 여 특정 키를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53075-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="53075-111">예제의</span><span class="sxs-lookup"><span data-stu-id="53075-111">EXAMPLES</span></span>

### <span data-ttu-id="53075-112">예제 1: 모든 키 자격 증명 모음 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="53075-112">Example 1: Get all Key Vault keys</span></span>
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

<span data-ttu-id="53075-113">이 명령은 SQL 관리 인스턴스의 모든 키 자격 증명 모음 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53075-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="53075-114">예제 2: 특정 키 보관소 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="53075-114">Example 2: Get a specific Key Vault key</span></span>
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

<span data-ttu-id="53075-115">이 명령은 Id가 ' ' 인 키 보관소 키를 가져옵니다 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="53075-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="53075-116">예제 3: 인스턴스 개체 사용</span><span class="sxs-lookup"><span data-stu-id="53075-116">Example 3: Using instance object</span></span>
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

<span data-ttu-id="53075-117">이 명령은 Id가 ' ' 인 키 보관소 키를 가져옵니다 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="53075-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="53075-118">예제 4: 인스턴스 리소스 id 사용</span><span class="sxs-lookup"><span data-stu-id="53075-118">Example 4: Using instance resource id</span></span>
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

<span data-ttu-id="53075-119">이 명령은 Id가 ' ' 인 키 보관소 키를 가져옵니다 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="53075-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="53075-120">예제 5: 파이핑 사용</span><span class="sxs-lookup"><span data-stu-id="53075-120">Example 5: Using piping</span></span>
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

<span data-ttu-id="53075-121">이 명령은 Id가 ' ' 인 키 보관소 키를 가져옵니다 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="53075-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="53075-122">변수</span><span class="sxs-lookup"><span data-stu-id="53075-122">PARAMETERS</span></span>

### <span data-ttu-id="53075-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53075-123">-DefaultProfile</span></span>
<span data-ttu-id="53075-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53075-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53075-125">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="53075-125">-Instance</span></span>
<span data-ttu-id="53075-126">인스턴스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="53075-126">The instance input object</span></span>

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

### <span data-ttu-id="53075-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="53075-127">-InstanceName</span></span>
<span data-ttu-id="53075-128">인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="53075-128">The instance name</span></span>

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

### <span data-ttu-id="53075-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="53075-129">-InstanceResourceId</span></span>
<span data-ttu-id="53075-130">인스턴스 리소스 id</span><span class="sxs-lookup"><span data-stu-id="53075-130">The instance resource id</span></span>

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

### <span data-ttu-id="53075-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="53075-131">-KeyId</span></span>
<span data-ttu-id="53075-132">AzureKeyVault 키 id</span><span class="sxs-lookup"><span data-stu-id="53075-132">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="53075-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53075-133">-ResourceGroupName</span></span>
<span data-ttu-id="53075-134">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="53075-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="53075-135">-확인</span><span class="sxs-lookup"><span data-stu-id="53075-135">-Confirm</span></span>
<span data-ttu-id="53075-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="53075-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53075-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53075-137">-WhatIf</span></span>
<span data-ttu-id="53075-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53075-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53075-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53075-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53075-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53075-140">CommonParameters</span></span>
<span data-ttu-id="53075-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53075-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53075-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53075-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53075-143">입력</span><span class="sxs-lookup"><span data-stu-id="53075-143">INPUTS</span></span>

### <span data-ttu-id="53075-144">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="53075-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="53075-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="53075-145">System.String</span></span>

## <span data-ttu-id="53075-146">출력</span><span class="sxs-lookup"><span data-stu-id="53075-146">OUTPUTS</span></span>

### <span data-ttu-id="53075-147">TransparentDataEncryption. AzureRmSqlManagedInstanceKeyVaultKeyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="53075-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="53075-148">상속자</span><span class="sxs-lookup"><span data-stu-id="53075-148">NOTES</span></span>

## <span data-ttu-id="53075-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53075-149">RELATED LINKS</span></span>
