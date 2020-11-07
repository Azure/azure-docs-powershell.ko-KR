---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 0321fc68c22e3bea973c25f9bbb27e0c5736e944
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873740"
---
# <span data-ttu-id="082fe-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="082fe-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="082fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="082fe-102">SYNOPSIS</span></span>
<span data-ttu-id="082fe-103">SQL 관리 인스턴스에 대 한 TDE (투명 한 데이터 암호화) 보호기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="082fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="082fe-104">SYNTAX</span></span>

### <span data-ttu-id="082fe-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="082fe-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="082fe-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="082fe-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="082fe-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="082fe-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="082fe-108">설명은</span><span class="sxs-lookup"><span data-stu-id="082fe-108">DESCRIPTION</span></span>
<span data-ttu-id="082fe-109">Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet은 SQL 관리 인스턴스에 대 한 TDE 프로텍터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="082fe-110">TDE 프로텍터 유형을 변경 하면 보호기가 회전 합니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="082fe-111">예제의</span><span class="sxs-lookup"><span data-stu-id="082fe-111">EXAMPLES</span></span>

### <span data-ttu-id="082fe-112">예제 1: ServiceManaged에 대 한 TDE (투명 데이터 암호화) 보호기 형식 설정</span><span class="sxs-lookup"><span data-stu-id="082fe-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="082fe-113">이 명령은 관리 되는 인스턴스의 TDE 프로텍터 형식을 서비스 관리로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="082fe-114">예제 2: 투명 한 데이터 암호화 보호기 유형을 Azure Key Vault로 설정</span><span class="sxs-lookup"><span data-stu-id="082fe-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="082fe-115">이 명령은 지정 된 관리 되는 인스턴스를 업데이트 하 여 Id가 ' ' 인 관리 되는 인스턴스 키 자격 증명 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE 프로텍터로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="082fe-116">예제 3: 관리 되는 인스턴스 개체를 사용 하 여 투명 한 데이터 암호화 보호기 유형을 Azure Key Vault로 설정</span><span class="sxs-lookup"><span data-stu-id="082fe-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="082fe-117">이 명령은 지정 된 관리 되는 인스턴스를 업데이트 하 여 Id가 ' ' 인 관리 되는 인스턴스 키 자격 증명 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE 프로텍터로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="082fe-118">예제 4: 리소스 id를 사용 하 여 투명 한 데이터 암호화 보호기 유형을 Azure 키 자격 증명 모음으로 설정</span><span class="sxs-lookup"><span data-stu-id="082fe-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="082fe-119">이 명령은 지정 된 관리 되는 인스턴스를 업데이트 하 여 Id가 ' ' 인 관리 되는 인스턴스 키 자격 증명 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE 프로텍터로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="082fe-120">예제 5: 파이핑를 사용 하 여 투명 한 데이터 암호화 보호기 유형을 Azure Key Vault로 설정</span><span class="sxs-lookup"><span data-stu-id="082fe-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="082fe-121">이 명령은 지정 된 관리 되는 인스턴스를 업데이트 하 여 Id가 ' ' 인 관리 되는 인스턴스 키 자격 증명 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE 프로텍터로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="082fe-122">변수</span><span class="sxs-lookup"><span data-stu-id="082fe-122">PARAMETERS</span></span>

### <span data-ttu-id="082fe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082fe-123">-DefaultProfile</span></span>
<span data-ttu-id="082fe-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="082fe-125">-Force</span><span class="sxs-lookup"><span data-stu-id="082fe-125">-Force</span></span>
<span data-ttu-id="082fe-126">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="082fe-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="082fe-127">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="082fe-127">-Instance</span></span>
<span data-ttu-id="082fe-128">인스턴스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="082fe-128">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="082fe-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="082fe-129">-InstanceName</span></span>
<span data-ttu-id="082fe-130">인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="082fe-130">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082fe-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="082fe-131">-InstanceResourceId</span></span>
<span data-ttu-id="082fe-132">인스턴스 리소스 id</span><span class="sxs-lookup"><span data-stu-id="082fe-132">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="082fe-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="082fe-133">-KeyId</span></span>
<span data-ttu-id="082fe-134">Azure 키 자격 증명 모음 KeyId.</span><span class="sxs-lookup"><span data-stu-id="082fe-134">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082fe-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="082fe-135">-ResourceGroupName</span></span>
<span data-ttu-id="082fe-136">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="082fe-136">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082fe-137">-Type</span><span class="sxs-lookup"><span data-stu-id="082fe-137">-Type</span></span>
<span data-ttu-id="082fe-138">Azure Sql 데이터베이스 투명 데이터 암호화 보호 기능 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082fe-139">-확인</span><span class="sxs-lookup"><span data-stu-id="082fe-139">-Confirm</span></span>
<span data-ttu-id="082fe-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="082fe-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="082fe-141">-WhatIf</span></span>
<span data-ttu-id="082fe-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="082fe-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="082fe-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082fe-144">CommonParameters</span></span>
<span data-ttu-id="082fe-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="082fe-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082fe-146">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="082fe-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082fe-147">입력</span><span class="sxs-lookup"><span data-stu-id="082fe-147">INPUTS</span></span>

### <span data-ttu-id="082fe-148">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="082fe-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="082fe-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="082fe-149">System.String</span></span>

## <span data-ttu-id="082fe-150">출력</span><span class="sxs-lookup"><span data-stu-id="082fe-150">OUTPUTS</span></span>

### <span data-ttu-id="082fe-151">TransparentDataEncryption. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="082fe-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="082fe-152">상속자</span><span class="sxs-lookup"><span data-stu-id="082fe-152">NOTES</span></span>

## <span data-ttu-id="082fe-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="082fe-153">RELATED LINKS</span></span>
