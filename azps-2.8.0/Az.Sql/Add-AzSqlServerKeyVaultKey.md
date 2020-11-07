---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 9b07a7d9113411b83c97818d6d34c5a7df40c8fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871458"
---
# <span data-ttu-id="7c71a-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7c71a-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="7c71a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c71a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c71a-103">SQL server에 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c71a-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="7c71a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c71a-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c71a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c71a-105">DESCRIPTION</span></span>
<span data-ttu-id="7c71a-106">Add-AzSqlServerKeyVaultKey cmdlet은 제공 된 SQL server에 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c71a-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="7c71a-107">서버에는 자격 증명 모음에 대 한 ' get, wrapKey, unwrapKey ' 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c71a-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="7c71a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7c71a-108">EXAMPLES</span></span>

### <span data-ttu-id="7c71a-109">예제 1: 키 자격 증명 모음 키 추가</span><span class="sxs-lookup"><span data-stu-id="7c71a-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="7c71a-110">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 리소스 그룹 ' ContosoResourceGroup '에서 이름이 ' ContosoServer ' 인 SQL server에 Id가 ' ' 인 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c71a-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="7c71a-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지문: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="7c71a-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="7c71a-112">변수</span><span class="sxs-lookup"><span data-stu-id="7c71a-112">PARAMETERS</span></span>

### <span data-ttu-id="7c71a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c71a-113">-AsJob</span></span>
<span data-ttu-id="7c71a-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c71a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c71a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c71a-115">-DefaultProfile</span></span>
<span data-ttu-id="7c71a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7c71a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c71a-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7c71a-117">-KeyId</span></span>
<span data-ttu-id="7c71a-118">Azure 키 자격 증명 모음 KeyId.</span><span class="sxs-lookup"><span data-stu-id="7c71a-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="7c71a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c71a-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c71a-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c71a-120">The name of the resource group</span></span>

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

### <span data-ttu-id="7c71a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7c71a-121">-ServerName</span></span>
<span data-ttu-id="7c71a-122">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c71a-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7c71a-123">-확인</span><span class="sxs-lookup"><span data-stu-id="7c71a-123">-Confirm</span></span>
<span data-ttu-id="7c71a-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c71a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c71a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c71a-125">-WhatIf</span></span>
<span data-ttu-id="7c71a-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c71a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c71a-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c71a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c71a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c71a-128">CommonParameters</span></span>
<span data-ttu-id="7c71a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c71a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c71a-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c71a-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c71a-131">입력</span><span class="sxs-lookup"><span data-stu-id="7c71a-131">INPUTS</span></span>

### <span data-ttu-id="7c71a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c71a-132">System.String</span></span>

## <span data-ttu-id="7c71a-133">출력</span><span class="sxs-lookup"><span data-stu-id="7c71a-133">OUTPUTS</span></span>

### <span data-ttu-id="7c71a-134">ServerKeyVaultKey. AzureSqlServerKeyVaultKeyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="7c71a-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="7c71a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="7c71a-135">NOTES</span></span>

## <span data-ttu-id="7c71a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c71a-136">RELATED LINKS</span></span>

[<span data-ttu-id="7c71a-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="7c71a-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
