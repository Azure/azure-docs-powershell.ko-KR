---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 81ec18dd543a63a971d01a64c878774b266cf0fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536503"
---
# <span data-ttu-id="22bb0-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="22bb0-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="22bb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="22bb0-103">SQL server에서 키 자격 증명 모음 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22bb0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22bb0-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22bb0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="22bb0-106">Remove-AzureRmSqlServerKeyVaultKey cmdlet은 지정 된 SQL server에서 키 자격 증명 모음 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="22bb0-107">키 보관소에 대 한 SQL server의 사용 권한은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="22bb0-108">사용 권한을 변경 하려면 Set-AzureRmKeyVaultAccessPolicy를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="22bb0-109">이 cmdlet은 키 자격 증명을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="22bb0-110">키 자격 증명 모음에서 키를 제거 하려면 AzureKeyVaultKey를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="22bb0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="22bb0-111">EXAMPLES</span></span>

### <span data-ttu-id="22bb0-112">예제 1: 키 자격 증명 모음 키 제거</span><span class="sxs-lookup"><span data-stu-id="22bb0-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="22bb0-113">이 명령은 지정 된 서버에서 Id가 ' ' 인 키 보관소 키를 제거 합니다 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="22bb0-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="22bb0-114">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지문: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="22bb0-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="22bb0-115">변수</span><span class="sxs-lookup"><span data-stu-id="22bb0-115">PARAMETERS</span></span>

### <span data-ttu-id="22bb0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22bb0-116">-AsJob</span></span>
<span data-ttu-id="22bb0-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="22bb0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22bb0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22bb0-118">-DefaultProfile</span></span>
<span data-ttu-id="22bb0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="22bb0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22bb0-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="22bb0-120">-KeyId</span></span>
<span data-ttu-id="22bb0-121">Azure 키 자격 증명 모음 KeyId.</span><span class="sxs-lookup"><span data-stu-id="22bb0-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="22bb0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22bb0-122">-ResourceGroupName</span></span>
<span data-ttu-id="22bb0-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-123">The name of the resource group</span></span>

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

### <span data-ttu-id="22bb0-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="22bb0-124">-ServerName</span></span>
<span data-ttu-id="22bb0-125">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="22bb0-126">-확인</span><span class="sxs-lookup"><span data-stu-id="22bb0-126">-Confirm</span></span>
<span data-ttu-id="22bb0-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22bb0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22bb0-128">-WhatIf</span></span>
<span data-ttu-id="22bb0-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22bb0-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22bb0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22bb0-131">CommonParameters</span></span>
<span data-ttu-id="22bb0-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22bb0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22bb0-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22bb0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22bb0-134">입력</span><span class="sxs-lookup"><span data-stu-id="22bb0-134">INPUTS</span></span>

### <span data-ttu-id="22bb0-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22bb0-135">System.String</span></span>

## <span data-ttu-id="22bb0-136">출력</span><span class="sxs-lookup"><span data-stu-id="22bb0-136">OUTPUTS</span></span>

### <span data-ttu-id="22bb0-137">ServerKeyVaultKey. AzureSqlServerKeyVaultKeyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="22bb0-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="22bb0-138">상속자</span><span class="sxs-lookup"><span data-stu-id="22bb0-138">NOTES</span></span>

## <span data-ttu-id="22bb0-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22bb0-139">RELATED LINKS</span></span>

[<span data-ttu-id="22bb0-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="22bb0-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
