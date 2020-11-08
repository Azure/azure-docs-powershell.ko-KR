---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213853"
---
# <span data-ttu-id="863e9-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="863e9-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="863e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="863e9-102">SYNOPSIS</span></span>
<span data-ttu-id="863e9-103">SQL server에 대 한 TDE (투명 한 데이터 암호화) 보호기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="863e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="863e9-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="863e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="863e9-105">DESCRIPTION</span></span>
<span data-ttu-id="863e9-106">Set-AzSqlServerTransparentDataEncryptionProtector cmdlet은 SQL server에 대 한 TDE 보호 기능을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="863e9-107">TDE 프로텍터 유형을 변경 하면 보호기가 회전 합니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="863e9-108">예제의</span><span class="sxs-lookup"><span data-stu-id="863e9-108">EXAMPLES</span></span>

### <span data-ttu-id="863e9-109">예제 1: ServiceManaged에 대 한 TDE (투명 데이터 암호화) 보호기 형식 설정</span><span class="sxs-lookup"><span data-stu-id="863e9-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="863e9-110">이 명령은 서버의 TDE 프로텍터 유형을 서비스 관리로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="863e9-111">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="863e9-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="863e9-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="863e9-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="863e9-113">예제 2: 투명 한 데이터 암호화 보호기 유형을 Azure Key Vault로 설정</span><span class="sxs-lookup"><span data-stu-id="863e9-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="863e9-114">이 명령은 TDE 프로텍터로 Id가 ' ' 인 서버 키 보관소 키를 사용 하도록 서버를 업데이트 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 합니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="863e9-115">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="863e9-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="863e9-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="863e9-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="863e9-117">변수</span><span class="sxs-lookup"><span data-stu-id="863e9-117">PARAMETERS</span></span>

### <span data-ttu-id="863e9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="863e9-118">-AsJob</span></span>
<span data-ttu-id="863e9-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="863e9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="863e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="863e9-120">-DefaultProfile</span></span>
<span data-ttu-id="863e9-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="863e9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="863e9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="863e9-122">-Force</span></span>
<span data-ttu-id="863e9-123">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="863e9-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="863e9-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="863e9-124">-KeyId</span></span>
<span data-ttu-id="863e9-125">Azure 키 자격 증명 모음 KeyId.</span><span class="sxs-lookup"><span data-stu-id="863e9-125">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="863e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="863e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="863e9-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-127">The name of the resource group</span></span>

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

### <span data-ttu-id="863e9-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="863e9-128">-ServerName</span></span>
<span data-ttu-id="863e9-129">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="863e9-130">-Type</span><span class="sxs-lookup"><span data-stu-id="863e9-130">-Type</span></span>
<span data-ttu-id="863e9-131">Azure Sql 데이터베이스 TDE 프로텍터 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-131">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="863e9-132">-확인</span><span class="sxs-lookup"><span data-stu-id="863e9-132">-Confirm</span></span>
<span data-ttu-id="863e9-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="863e9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="863e9-134">-WhatIf</span></span>
<span data-ttu-id="863e9-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="863e9-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="863e9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="863e9-137">CommonParameters</span></span>
<span data-ttu-id="863e9-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="863e9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="863e9-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="863e9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="863e9-140">입력</span><span class="sxs-lookup"><span data-stu-id="863e9-140">INPUTS</span></span>

### <span data-ttu-id="863e9-141">TransparentDataEncryption. EncryptionProtectorType에 대 한</span><span class="sxs-lookup"><span data-stu-id="863e9-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="863e9-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="863e9-142">System.String</span></span>

## <span data-ttu-id="863e9-143">출력</span><span class="sxs-lookup"><span data-stu-id="863e9-143">OUTPUTS</span></span>

### <span data-ttu-id="863e9-144">TransparentDataEncryption. AzureSqlServerTransparentDataEncryptionProtectorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="863e9-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="863e9-145">상속자</span><span class="sxs-lookup"><span data-stu-id="863e9-145">NOTES</span></span>

## <span data-ttu-id="863e9-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="863e9-146">RELATED LINKS</span></span>

[<span data-ttu-id="863e9-147">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="863e9-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
