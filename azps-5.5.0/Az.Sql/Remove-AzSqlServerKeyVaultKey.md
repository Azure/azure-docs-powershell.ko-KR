---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197652"
---
# <span data-ttu-id="cb5c4-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cb5c4-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="cb5c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5c4-103">키 자격 증명 모음 키는 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="cb5c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb5c4-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb5c4-105">설명</span><span class="sxs-lookup"><span data-stu-id="cb5c4-105">DESCRIPTION</span></span>
<span data-ttu-id="cb5c4-106">Remove-AzSqlServerKeyVaultKey cmdlet은 지정된 서버의 Key Vault SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="cb5c4-107">키의 SQL 서버의 권한은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="cb5c4-108">사용 권한을 변경하려면 Set-AzKeyVaultAccessPolicy를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="cb5c4-109">이 cmdlet은 Key Vault를 변경하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="cb5c4-110">Key Vault에서 키를 제거하려면 Remove-AzKeyVaultKey를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="cb5c4-111">예제</span><span class="sxs-lookup"><span data-stu-id="cb5c4-111">EXAMPLES</span></span>

### <span data-ttu-id="cb5c4-112">예제 1: Key Vault 키 제거</span><span class="sxs-lookup"><span data-stu-id="cb5c4-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="cb5c4-113">이 명령은 지정된 서버에서 ID '를 사용하여 Key Vault 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="cb5c4-114">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 11223344556677889900112223344556677889900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="cb5c4-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="cb5c4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb5c4-115">PARAMETERS</span></span>

### <span data-ttu-id="cb5c4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb5c4-116">-AsJob</span></span>
<span data-ttu-id="cb5c4-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cb5c4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb5c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5c4-118">-DefaultProfile</span></span>
<span data-ttu-id="cb5c4-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cb5c4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb5c4-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="cb5c4-120">-KeyId</span></span>
<span data-ttu-id="cb5c4-121">Azure Key Vault KeyId입니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb5c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb5c4-123">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="cb5c4-123">The name of the resource group</span></span>

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

### <span data-ttu-id="cb5c4-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb5c4-124">-ServerName</span></span>
<span data-ttu-id="cb5c4-125">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="cb5c4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb5c4-126">-Confirm</span></span>
<span data-ttu-id="cb5c4-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb5c4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb5c4-128">-WhatIf</span></span>
<span data-ttu-id="cb5c4-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cb5c4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb5c4-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb5c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5c4-131">CommonParameters</span></span>
<span data-ttu-id="cb5c4-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5c4-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb5c4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5c4-134">입력</span><span class="sxs-lookup"><span data-stu-id="cb5c4-134">INPUTS</span></span>

### <span data-ttu-id="cb5c4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="cb5c4-135">System.String</span></span>

## <span data-ttu-id="cb5c4-136">출력</span><span class="sxs-lookup"><span data-stu-id="cb5c4-136">OUTPUTS</span></span>

### <span data-ttu-id="cb5c4-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="cb5c4-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="cb5c4-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb5c4-138">NOTES</span></span>

## <span data-ttu-id="cb5c4-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb5c4-139">RELATED LINKS</span></span>

[<span data-ttu-id="cb5c4-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="cb5c4-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
