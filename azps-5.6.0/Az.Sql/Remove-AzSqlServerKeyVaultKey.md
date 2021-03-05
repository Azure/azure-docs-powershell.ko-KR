---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 5b394909df0469c37a0217b3eb861ce4a1146e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967344"
---
# <span data-ttu-id="f2b45-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f2b45-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="f2b45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2b45-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b45-103">키 자격 증명 모음 키를 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="f2b45-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2b45-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b45-105">설명</span><span class="sxs-lookup"><span data-stu-id="f2b45-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b45-106">Remove-AzSqlServerKeyVaultKey cmdlet은 지정된 SQL 키 자격 증명 모음 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="f2b45-107">키의 SQL 서버의 사용 권한은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="f2b45-108">사용 권한을 변경하려면 Set-AzKeyVaultAccessPolicy를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="f2b45-109">이 cmdlet은 Key Vault를 변경하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="f2b45-110">Key Vault에서 키를 제거하려면 Remove-AzKeyVaultKey를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="f2b45-111">예제</span><span class="sxs-lookup"><span data-stu-id="f2b45-111">EXAMPLES</span></span>

### <span data-ttu-id="f2b45-112">예제 1: Key Vault 키 제거</span><span class="sxs-lookup"><span data-stu-id="f2b45-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="f2b45-113">이 명령은 지정된 서버에서 Id ''를 사용하여 Key Vault 키를 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="f2b45-114">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 형식 : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지문 : 1122334556677889001122334556778900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="f2b45-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="f2b45-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f2b45-115">PARAMETERS</span></span>

### <span data-ttu-id="f2b45-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2b45-116">-AsJob</span></span>
<span data-ttu-id="f2b45-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f2b45-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2b45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b45-118">-DefaultProfile</span></span>
<span data-ttu-id="f2b45-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f2b45-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2b45-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f2b45-120">-KeyId</span></span>
<span data-ttu-id="f2b45-121">Azure Key Vault KeyId입니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="f2b45-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b45-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2b45-123">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="f2b45-123">The name of the resource group</span></span>

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

### <span data-ttu-id="f2b45-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f2b45-124">-ServerName</span></span>
<span data-ttu-id="f2b45-125">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="f2b45-126">-확인</span><span class="sxs-lookup"><span data-stu-id="f2b45-126">-Confirm</span></span>
<span data-ttu-id="f2b45-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b45-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b45-128">-WhatIf</span></span>
<span data-ttu-id="f2b45-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b45-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b45-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b45-131">CommonParameters</span></span>
<span data-ttu-id="f2b45-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b45-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b45-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2b45-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b45-134">입력</span><span class="sxs-lookup"><span data-stu-id="f2b45-134">INPUTS</span></span>

### <span data-ttu-id="f2b45-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f2b45-135">System.String</span></span>

## <span data-ttu-id="f2b45-136">출력</span><span class="sxs-lookup"><span data-stu-id="f2b45-136">OUTPUTS</span></span>

### <span data-ttu-id="f2b45-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="f2b45-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="f2b45-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2b45-138">NOTES</span></span>

## <span data-ttu-id="f2b45-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2b45-139">RELATED LINKS</span></span>

[<span data-ttu-id="f2b45-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f2b45-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
