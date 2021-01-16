---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333254"
---
# <span data-ttu-id="933b0-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="933b0-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="933b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="933b0-102">SYNOPSIS</span></span>
<span data-ttu-id="933b0-103">서버의 TDE(투명한 데이터 암호화) 보호 SQL.</span><span class="sxs-lookup"><span data-stu-id="933b0-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="933b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="933b0-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="933b0-105">설명</span><span class="sxs-lookup"><span data-stu-id="933b0-105">DESCRIPTION</span></span>
<span data-ttu-id="933b0-106">Set-AzSqlServerTransparentDataEncryptionProtector cmdlet은 SQL 서버에 대한 TDE 보호기 SQL 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="933b0-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="933b0-107">TDE 보호기 유형을 변경하면 보호기 회전이 회전됩니다.</span><span class="sxs-lookup"><span data-stu-id="933b0-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="933b0-108">예제</span><span class="sxs-lookup"><span data-stu-id="933b0-108">EXAMPLES</span></span>

### <span data-ttu-id="933b0-109">예제 1: TDE(투명한 데이터 암호화) 보호기 유형을 ServiceManaged로 설정</span><span class="sxs-lookup"><span data-stu-id="933b0-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="933b0-110">이 명령은 서버의 TDE 보호기 유형을 서비스 관리로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="933b0-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="933b0-111">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="933b0-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="933b0-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="933b0-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="933b0-113">예제 2: 투명한 데이터 암호화 보호기 형식을 Azure Key Vault로 설정</span><span class="sxs-lookup"><span data-stu-id="933b0-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="933b0-114">이 명령은 서버 키 자격 증명 모음 키와 ID '를 TDE 보호기로 사용하여 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="933b0-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="933b0-115">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="933b0-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="933b0-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="933b0-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="933b0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="933b0-117">PARAMETERS</span></span>

### <span data-ttu-id="933b0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="933b0-118">-AsJob</span></span>
<span data-ttu-id="933b0-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="933b0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="933b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933b0-120">-DefaultProfile</span></span>
<span data-ttu-id="933b0-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="933b0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="933b0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="933b0-122">-Force</span></span>
<span data-ttu-id="933b0-123">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="933b0-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="933b0-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="933b0-124">-KeyId</span></span>
<span data-ttu-id="933b0-125">Azure Key Vault KeyId입니다.</span><span class="sxs-lookup"><span data-stu-id="933b0-125">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="933b0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933b0-126">-ResourceGroupName</span></span>
<span data-ttu-id="933b0-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="933b0-127">The name of the resource group</span></span>

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

### <span data-ttu-id="933b0-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="933b0-128">-ServerName</span></span>
<span data-ttu-id="933b0-129">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="933b0-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="933b0-130">-Type</span><span class="sxs-lookup"><span data-stu-id="933b0-130">-Type</span></span>
<span data-ttu-id="933b0-131">Azure Sql Database TDE 보호기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="933b0-131">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="933b0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="933b0-132">-Confirm</span></span>
<span data-ttu-id="933b0-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="933b0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="933b0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="933b0-134">-WhatIf</span></span>
<span data-ttu-id="933b0-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="933b0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="933b0-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="933b0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="933b0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933b0-137">CommonParameters</span></span>
<span data-ttu-id="933b0-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="933b0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933b0-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="933b0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933b0-140">입력</span><span class="sxs-lookup"><span data-stu-id="933b0-140">INPUTS</span></span>

### <span data-ttu-id="933b0-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="933b0-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="933b0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="933b0-142">System.String</span></span>

## <span data-ttu-id="933b0-143">출력</span><span class="sxs-lookup"><span data-stu-id="933b0-143">OUTPUTS</span></span>

### <span data-ttu-id="933b0-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="933b0-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="933b0-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="933b0-145">NOTES</span></span>

## <span data-ttu-id="933b0-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="933b0-146">RELATED LINKS</span></span>

[<span data-ttu-id="933b0-147">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="933b0-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
