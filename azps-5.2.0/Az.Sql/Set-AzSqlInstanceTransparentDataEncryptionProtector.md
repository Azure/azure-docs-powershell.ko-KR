---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348597"
---
# <span data-ttu-id="1ddcf-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1ddcf-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="1ddcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ddcf-102">SYNOPSIS</span></span>
<span data-ttu-id="1ddcf-103">관리되는 인스턴스에 대해 TDE(투명한 데이터 암호화) 보호 SQL 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="1ddcf-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ddcf-104">SYNTAX</span></span>

### <span data-ttu-id="1ddcf-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1ddcf-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ddcf-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ddcf-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ddcf-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ddcf-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ddcf-108">설명</span><span class="sxs-lookup"><span data-stu-id="1ddcf-108">DESCRIPTION</span></span>
<span data-ttu-id="1ddcf-109">Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet은 관리되는 인스턴스에 대한 TDE SQL 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="1ddcf-110">TDE 보호기 유형을 변경하면 보호기 회전이 회전됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="1ddcf-111">예제</span><span class="sxs-lookup"><span data-stu-id="1ddcf-111">EXAMPLES</span></span>

### <span data-ttu-id="1ddcf-112">예제 1: TDE(투명한 데이터 암호화) 보호기 유형을 ServiceManaged로 설정</span><span class="sxs-lookup"><span data-stu-id="1ddcf-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="1ddcf-113">이 명령은 관리되는 인스턴스의 TDE 보호기 유형을 서비스 관리형으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="1ddcf-114">예제 2: 투명한 데이터 암호화 보호기 형식을 Azure Key Vault로 설정</span><span class="sxs-lookup"><span data-stu-id="1ddcf-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="1ddcf-115">이 명령은 지정된 관리되는 인스턴스를 업데이트하여 ID '를 TDE 보호기로 사용하여 Managed Instance Key Vault 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="1ddcf-116">예제 3: 관리되는 인스턴스 개체를 사용하여 투명한 데이터 암호화 보호기 형식을 Azure Key Vault로 설정</span><span class="sxs-lookup"><span data-stu-id="1ddcf-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="1ddcf-117">이 명령은 지정된 관리되는 인스턴스를 업데이트하여 ID '를 TDE 보호기로 사용하여 Managed Instance Key Vault 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="1ddcf-118">예제 4: 리소스 ID를 사용하여 투명한 데이터 암호화 보호기 형식을 Azure Key Vault로 설정</span><span class="sxs-lookup"><span data-stu-id="1ddcf-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="1ddcf-119">이 명령은 지정된 관리되는 인스턴스를 업데이트하여 ID '를 TDE 보호기로 사용하여 Managed Instance Key Vault 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="1ddcf-120">예제 5: 파이핑을 사용하여 투명한 데이터 암호화 보호기 형식을 Azure Key Vault로 설정</span><span class="sxs-lookup"><span data-stu-id="1ddcf-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="1ddcf-121">이 명령은 지정된 관리되는 인스턴스를 업데이트하여 ID '를 TDE 보호기로 사용하여 Managed Instance Key Vault 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="1ddcf-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ddcf-122">PARAMETERS</span></span>

### <span data-ttu-id="1ddcf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ddcf-123">-DefaultProfile</span></span>
<span data-ttu-id="1ddcf-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ddcf-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1ddcf-125">-Force</span></span>
<span data-ttu-id="1ddcf-126">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="1ddcf-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1ddcf-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="1ddcf-127">-Instance</span></span>
<span data-ttu-id="1ddcf-128">인스턴스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="1ddcf-128">The instance input object</span></span>

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

### <span data-ttu-id="1ddcf-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1ddcf-129">-InstanceName</span></span>
<span data-ttu-id="1ddcf-130">인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="1ddcf-130">The instance name</span></span>

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

### <span data-ttu-id="1ddcf-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="1ddcf-131">-InstanceResourceId</span></span>
<span data-ttu-id="1ddcf-132">인스턴스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1ddcf-132">The instance resource id</span></span>

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

### <span data-ttu-id="1ddcf-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="1ddcf-133">-KeyId</span></span>
<span data-ttu-id="1ddcf-134">Azure Key Vault KeyId입니다.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-134">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="1ddcf-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ddcf-135">-ResourceGroupName</span></span>
<span data-ttu-id="1ddcf-136">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1ddcf-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="1ddcf-137">-Type</span><span class="sxs-lookup"><span data-stu-id="1ddcf-137">-Type</span></span>
<span data-ttu-id="1ddcf-138">Azure Sql Database 투명한 데이터 암호화 보호기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

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

### <span data-ttu-id="1ddcf-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ddcf-139">-Confirm</span></span>
<span data-ttu-id="1ddcf-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ddcf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ddcf-141">-WhatIf</span></span>
<span data-ttu-id="1ddcf-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1ddcf-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ddcf-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ddcf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ddcf-144">CommonParameters</span></span>
<span data-ttu-id="1ddcf-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ddcf-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ddcf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ddcf-147">입력</span><span class="sxs-lookup"><span data-stu-id="1ddcf-147">INPUTS</span></span>

### <span data-ttu-id="1ddcf-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="1ddcf-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="1ddcf-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1ddcf-149">System.String</span></span>

## <span data-ttu-id="1ddcf-150">출력</span><span class="sxs-lookup"><span data-stu-id="1ddcf-150">OUTPUTS</span></span>

### <span data-ttu-id="1ddcf-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="1ddcf-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="1ddcf-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ddcf-152">NOTES</span></span>

## <span data-ttu-id="1ddcf-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ddcf-153">RELATED LINKS</span></span>
