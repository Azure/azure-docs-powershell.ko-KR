---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 992601b3a6d88c7aa424564189dc8af3efe6464d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967280"
---
# <span data-ttu-id="575bb-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="575bb-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="575bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="575bb-102">SYNOPSIS</span></span>
<span data-ttu-id="575bb-103">TDE(투명한 데이터 암호화) 보호구를 서버의 SQL 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="575bb-104">구문</span><span class="sxs-lookup"><span data-stu-id="575bb-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="575bb-105">설명</span><span class="sxs-lookup"><span data-stu-id="575bb-105">DESCRIPTION</span></span>
<span data-ttu-id="575bb-106">Set-AzSqlServerTransparentDataEncryptionProtector cmdlet은 SQL TDE 보호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="575bb-107">TDE 보호기 유형을 변경하면 보호가 회전됩니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="575bb-108">예제</span><span class="sxs-lookup"><span data-stu-id="575bb-108">EXAMPLES</span></span>

### <span data-ttu-id="575bb-109">예제 1: TDE(투명한 데이터 암호화) 보호자 형식을 ServiceManaged로 설정</span><span class="sxs-lookup"><span data-stu-id="575bb-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="575bb-110">이 명령은 서버의 TDE 보호자 유형을 Service Managed로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="575bb-111">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="575bb-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="575bb-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="575bb-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="575bb-113">예제 2: 투명한 데이터 암호화 보호자 형식을 Azure Key Vault로 설정</span><span class="sxs-lookup"><span data-stu-id="575bb-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="575bb-114">이 명령은 서버를 업데이트하여 Id ''가 있는 서버 키 자격 증명 모음 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE 보호기로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="575bb-115">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="575bb-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="575bb-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="575bb-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="575bb-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="575bb-117">PARAMETERS</span></span>

### <span data-ttu-id="575bb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="575bb-118">-AsJob</span></span>
<span data-ttu-id="575bb-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="575bb-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="575bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575bb-120">-DefaultProfile</span></span>
<span data-ttu-id="575bb-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="575bb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="575bb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="575bb-122">-Force</span></span>
<span data-ttu-id="575bb-123">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="575bb-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="575bb-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="575bb-124">-KeyId</span></span>
<span data-ttu-id="575bb-125">Azure Key Vault KeyId입니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575bb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="575bb-126">-ResourceGroupName</span></span>
<span data-ttu-id="575bb-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="575bb-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575bb-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="575bb-128">-ServerName</span></span>
<span data-ttu-id="575bb-129">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575bb-130">-Type</span><span class="sxs-lookup"><span data-stu-id="575bb-130">-Type</span></span>
<span data-ttu-id="575bb-131">Azure Sql Database TDE 보호자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575bb-132">-확인</span><span class="sxs-lookup"><span data-stu-id="575bb-132">-Confirm</span></span>
<span data-ttu-id="575bb-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575bb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="575bb-134">-WhatIf</span></span>
<span data-ttu-id="575bb-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="575bb-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575bb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575bb-137">CommonParameters</span></span>
<span data-ttu-id="575bb-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="575bb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575bb-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="575bb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575bb-140">입력</span><span class="sxs-lookup"><span data-stu-id="575bb-140">INPUTS</span></span>

### <span data-ttu-id="575bb-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="575bb-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="575bb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="575bb-142">System.String</span></span>

## <span data-ttu-id="575bb-143">출력</span><span class="sxs-lookup"><span data-stu-id="575bb-143">OUTPUTS</span></span>

### <span data-ttu-id="575bb-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="575bb-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="575bb-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="575bb-145">NOTES</span></span>

## <span data-ttu-id="575bb-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="575bb-146">RELATED LINKS</span></span>

[<span data-ttu-id="575bb-147">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="575bb-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
