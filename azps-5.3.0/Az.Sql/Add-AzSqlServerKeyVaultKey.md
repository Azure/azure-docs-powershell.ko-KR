---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375565"
---
# <span data-ttu-id="628f1-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="628f1-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="628f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="628f1-102">SYNOPSIS</span></span>
<span data-ttu-id="628f1-103">Key Vault 키를 SQL 서버에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="628f1-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="628f1-104">구문</span><span class="sxs-lookup"><span data-stu-id="628f1-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="628f1-105">설명</span><span class="sxs-lookup"><span data-stu-id="628f1-105">DESCRIPTION</span></span>
<span data-ttu-id="628f1-106">Add-AzSqlServerKeyVaultKey cmdlet은 제공된 자격 증명 모음 서버에 Key Vault SQL 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="628f1-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="628f1-107">서버에 자격 증명 모음에 대한 'get, wrapKey, unwrapKey' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="628f1-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="628f1-108">예제</span><span class="sxs-lookup"><span data-stu-id="628f1-108">EXAMPLES</span></span>

### <span data-ttu-id="628f1-109">예제 1: Key Vault 키 추가</span><span class="sxs-lookup"><span data-stu-id="628f1-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="628f1-110">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoResourceGroup' 리소스 그룹의 'ContosoServer'라는 SQL 서버에 ID '가 있는 Key Vault 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="628f1-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="628f1-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 11223344556677889900112223344556677889900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="628f1-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="628f1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="628f1-112">PARAMETERS</span></span>

### <span data-ttu-id="628f1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="628f1-113">-AsJob</span></span>
<span data-ttu-id="628f1-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="628f1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="628f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="628f1-115">-DefaultProfile</span></span>
<span data-ttu-id="628f1-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="628f1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="628f1-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="628f1-117">-KeyId</span></span>
<span data-ttu-id="628f1-118">Azure Key Vault KeyId입니다.</span><span class="sxs-lookup"><span data-stu-id="628f1-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="628f1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="628f1-119">-ResourceGroupName</span></span>
<span data-ttu-id="628f1-120">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="628f1-120">The name of the resource group</span></span>

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

### <span data-ttu-id="628f1-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="628f1-121">-ServerName</span></span>
<span data-ttu-id="628f1-122">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="628f1-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="628f1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="628f1-123">-Confirm</span></span>
<span data-ttu-id="628f1-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="628f1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="628f1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="628f1-125">-WhatIf</span></span>
<span data-ttu-id="628f1-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="628f1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="628f1-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="628f1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="628f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="628f1-128">CommonParameters</span></span>
<span data-ttu-id="628f1-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="628f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="628f1-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="628f1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="628f1-131">입력</span><span class="sxs-lookup"><span data-stu-id="628f1-131">INPUTS</span></span>

### <span data-ttu-id="628f1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="628f1-132">System.String</span></span>

## <span data-ttu-id="628f1-133">출력</span><span class="sxs-lookup"><span data-stu-id="628f1-133">OUTPUTS</span></span>

### <span data-ttu-id="628f1-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="628f1-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="628f1-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="628f1-135">NOTES</span></span>

## <span data-ttu-id="628f1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="628f1-136">RELATED LINKS</span></span>

[<span data-ttu-id="628f1-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="628f1-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
