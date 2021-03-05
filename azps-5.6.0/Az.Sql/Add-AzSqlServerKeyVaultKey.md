---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f354fe8ad1876eb756cdf78378dbf7048e53932d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961472"
---
# <span data-ttu-id="5d714-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d714-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="5d714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d714-102">SYNOPSIS</span></span>
<span data-ttu-id="5d714-103">키 자격 증명 모음 키를 SQL 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d714-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="5d714-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d714-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d714-105">설명</span><span class="sxs-lookup"><span data-stu-id="5d714-105">DESCRIPTION</span></span>
<span data-ttu-id="5d714-106">Add-AzSqlServerKeyVaultKey cmdlet은 제공된 서버 서버에 Key Vault 키를 SQL 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d714-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="5d714-107">서버에는 자격 증명 모음에 대한 'get, wrapKey, unwrapKey' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d714-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="5d714-108">예제</span><span class="sxs-lookup"><span data-stu-id="5d714-108">EXAMPLES</span></span>

### <span data-ttu-id="5d714-109">예제 1: Key Vault 키 추가</span><span class="sxs-lookup"><span data-stu-id="5d714-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="5d714-110">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoResourceGroup'의 리소스 SQL 'ContosoServer'라는 이름의 서버에 Id ''를 사용하여 Key Vault 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d714-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="5d714-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 형식 : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지문 : 1122334556677889001122334556778900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="5d714-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="5d714-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d714-112">PARAMETERS</span></span>

### <span data-ttu-id="5d714-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d714-113">-AsJob</span></span>
<span data-ttu-id="5d714-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5d714-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d714-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d714-115">-DefaultProfile</span></span>
<span data-ttu-id="5d714-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5d714-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d714-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="5d714-117">-KeyId</span></span>
<span data-ttu-id="5d714-118">Azure Key Vault KeyId입니다.</span><span class="sxs-lookup"><span data-stu-id="5d714-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="5d714-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d714-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d714-120">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="5d714-120">The name of the resource group</span></span>

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

### <span data-ttu-id="5d714-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5d714-121">-ServerName</span></span>
<span data-ttu-id="5d714-122">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d714-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5d714-123">-확인</span><span class="sxs-lookup"><span data-stu-id="5d714-123">-Confirm</span></span>
<span data-ttu-id="5d714-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d714-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d714-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d714-125">-WhatIf</span></span>
<span data-ttu-id="5d714-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d714-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d714-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d714-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d714-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d714-128">CommonParameters</span></span>
<span data-ttu-id="5d714-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d714-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d714-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d714-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d714-131">입력</span><span class="sxs-lookup"><span data-stu-id="5d714-131">INPUTS</span></span>

### <span data-ttu-id="5d714-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5d714-132">System.String</span></span>

## <span data-ttu-id="5d714-133">출력</span><span class="sxs-lookup"><span data-stu-id="5d714-133">OUTPUTS</span></span>

### <span data-ttu-id="5d714-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="5d714-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="5d714-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d714-135">NOTES</span></span>

## <span data-ttu-id="5d714-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d714-136">RELATED LINKS</span></span>

[<span data-ttu-id="5d714-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5d714-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
