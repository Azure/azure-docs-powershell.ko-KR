---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369020"
---
# <span data-ttu-id="43d42-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43d42-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="43d42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d42-102">SYNOPSIS</span></span>
<span data-ttu-id="43d42-103">서버의 SQL 자격 증명 모음 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="43d42-104">구문</span><span class="sxs-lookup"><span data-stu-id="43d42-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43d42-105">설명</span><span class="sxs-lookup"><span data-stu-id="43d42-105">DESCRIPTION</span></span>
<span data-ttu-id="43d42-106">Get-AzSqlServerKeyVaultKey cmdlet은 SQL 서버의 Key Vault 키에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="43d42-107">KeyId를 제공하여 서버의 모든 키를 보거나 특정 키를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="43d42-108">예제</span><span class="sxs-lookup"><span data-stu-id="43d42-108">EXAMPLES</span></span>

### <span data-ttu-id="43d42-109">예제 1: 모든 Key Vault 키 얻기</span><span class="sxs-lookup"><span data-stu-id="43d42-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="43d42-110">이 명령은 서버의 모든 Key Vault 키를 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="43d42-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 11223344556677889900112223344556677889900 CreationDate : 1/1/2017 12:00:00 AM 리소스GroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey2_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint : 009988776655443321100998776554433221 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="43d42-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="43d42-112">예제 2: 특정 Key Vault 키 얻기</span><span class="sxs-lookup"><span data-stu-id="43d42-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="43d42-113">이 명령은 Id '를 사용하여 Key Vault 키를 $MyServerKeyVaultKey https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="43d42-114">키 자격 증명 모음에 대한 세부 정보를 $MyServerKeyVaultKey 속성이 검사될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="43d42-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43d42-115">PARAMETERS</span></span>

### <span data-ttu-id="43d42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d42-116">-DefaultProfile</span></span>
<span data-ttu-id="43d42-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="43d42-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43d42-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="43d42-118">-KeyId</span></span>
<span data-ttu-id="43d42-119">Azure Key Vault KeyId입니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-119">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43d42-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d42-120">-ResourceGroupName</span></span>
<span data-ttu-id="43d42-121">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="43d42-121">The name of the resource group</span></span>

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

### <span data-ttu-id="43d42-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="43d42-122">-ServerName</span></span>
<span data-ttu-id="43d42-123">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="43d42-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43d42-124">-Confirm</span></span>
<span data-ttu-id="43d42-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43d42-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43d42-126">-WhatIf</span></span>
<span data-ttu-id="43d42-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="43d42-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43d42-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43d42-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d42-129">CommonParameters</span></span>
<span data-ttu-id="43d42-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43d42-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d42-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43d42-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d42-132">입력</span><span class="sxs-lookup"><span data-stu-id="43d42-132">INPUTS</span></span>

### <span data-ttu-id="43d42-133">System.String</span><span class="sxs-lookup"><span data-stu-id="43d42-133">System.String</span></span>

## <span data-ttu-id="43d42-134">출력</span><span class="sxs-lookup"><span data-stu-id="43d42-134">OUTPUTS</span></span>

### <span data-ttu-id="43d42-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="43d42-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="43d42-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43d42-136">NOTES</span></span>

## <span data-ttu-id="43d42-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43d42-137">RELATED LINKS</span></span>

[<span data-ttu-id="43d42-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="43d42-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
