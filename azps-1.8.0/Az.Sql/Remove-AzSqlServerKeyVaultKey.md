---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: dcb099a26fe46325b1c3869b5e507347c948f09f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698826"
---
# <span data-ttu-id="901f4-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="901f4-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="901f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="901f4-102">SYNOPSIS</span></span>
<span data-ttu-id="901f4-103">SQL server에서 키 자격 증명 모음 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="901f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="901f4-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="901f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="901f4-105">DESCRIPTION</span></span>
<span data-ttu-id="901f4-106">Remove-AzSqlServerKeyVaultKey cmdlet은 지정 된 SQL server에서 키 자격 증명 모음 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="901f4-107">키 보관소에 대 한 SQL server의 사용 권한은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="901f4-108">사용 권한을 변경 하려면 Set-AzKeyVaultAccessPolicy를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="901f4-109">이 cmdlet은 키 자격 증명을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="901f4-110">키 자격 증명 모음에서 키를 제거 하려면 AzKeyVaultKey를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="901f4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="901f4-111">EXAMPLES</span></span>

### <span data-ttu-id="901f4-112">예제 1: 키 자격 증명 모음 키 제거</span><span class="sxs-lookup"><span data-stu-id="901f4-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="901f4-113">이 명령은 지정 된 서버에서 Id가 ' ' 인 키 보관소 키를 제거 합니다 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="901f4-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="901f4-114">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지문: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="901f4-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="901f4-115">변수</span><span class="sxs-lookup"><span data-stu-id="901f4-115">PARAMETERS</span></span>

### <span data-ttu-id="901f4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="901f4-116">-AsJob</span></span>
<span data-ttu-id="901f4-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="901f4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="901f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901f4-118">-DefaultProfile</span></span>
<span data-ttu-id="901f4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="901f4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="901f4-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="901f4-120">-KeyId</span></span>
<span data-ttu-id="901f4-121">Azure 키 자격 증명 모음 KeyId.</span><span class="sxs-lookup"><span data-stu-id="901f4-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="901f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="901f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="901f4-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-123">The name of the resource group</span></span>

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

### <span data-ttu-id="901f4-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="901f4-124">-ServerName</span></span>
<span data-ttu-id="901f4-125">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="901f4-126">-확인</span><span class="sxs-lookup"><span data-stu-id="901f4-126">-Confirm</span></span>
<span data-ttu-id="901f4-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="901f4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="901f4-128">-WhatIf</span></span>
<span data-ttu-id="901f4-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="901f4-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="901f4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901f4-131">CommonParameters</span></span>
<span data-ttu-id="901f4-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="901f4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901f4-133">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="901f4-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901f4-134">입력</span><span class="sxs-lookup"><span data-stu-id="901f4-134">INPUTS</span></span>

### <span data-ttu-id="901f4-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="901f4-135">System.String</span></span>

## <span data-ttu-id="901f4-136">출력</span><span class="sxs-lookup"><span data-stu-id="901f4-136">OUTPUTS</span></span>

### <span data-ttu-id="901f4-137">ServerKeyVaultKey. AzureSqlServerKeyVaultKeyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="901f4-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="901f4-138">상속자</span><span class="sxs-lookup"><span data-stu-id="901f4-138">NOTES</span></span>

## <span data-ttu-id="901f4-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="901f4-139">RELATED LINKS</span></span>

[<span data-ttu-id="901f4-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="901f4-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
