---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: b9051f8729ae1cee8216de5d2dab6d5ceb79a717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536944"
---
# <span data-ttu-id="d194e-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d194e-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="d194e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d194e-102">SYNOPSIS</span></span>
<span data-ttu-id="d194e-103">SQL server에 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d194e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d194e-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d194e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d194e-105">DESCRIPTION</span></span>
<span data-ttu-id="d194e-106">Add-AzureRmSqlServerKeyVaultKey cmdlet은 제공 된 SQL server에 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="d194e-107">서버에는 자격 증명 모음에 대 한 ' get, wrapKey, unwrapKey ' 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="d194e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d194e-108">EXAMPLES</span></span>

### <span data-ttu-id="d194e-109">--------------------------예제 1: 키 자격 증명 모음 키--------------------------추가</span><span class="sxs-lookup"><span data-stu-id="d194e-109">--------------------------  Example 1: Add Key Vault key  --------------------------</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="d194e-110">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 리소스 그룹 ' ContosoResourceGroup '에서 이름이 ' ContosoServer ' 인 SQL server에 Id가 ' ' 인 키 보관소 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="d194e-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지문: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="d194e-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="d194e-112">변수</span><span class="sxs-lookup"><span data-stu-id="d194e-112">PARAMETERS</span></span>

### <span data-ttu-id="d194e-113">-KeyId</span><span class="sxs-lookup"><span data-stu-id="d194e-113">-KeyId</span></span>
<span data-ttu-id="d194e-114">Azure 키 자격 증명 모음 KeyId.</span><span class="sxs-lookup"><span data-stu-id="d194e-114">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="d194e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d194e-115">-ResourceGroupName</span></span>
<span data-ttu-id="d194e-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-116">The name of the resource group</span></span>

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

### <span data-ttu-id="d194e-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d194e-117">-ServerName</span></span>
<span data-ttu-id="d194e-118">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d194e-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d194e-119">-Confirm</span></span>
<span data-ttu-id="d194e-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d194e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d194e-121">-WhatIf</span></span>
<span data-ttu-id="d194e-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d194e-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d194e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d194e-124">-DefaultProfile</span></span>
<span data-ttu-id="d194e-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d194e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d194e-126">CommonParameters</span></span>
<span data-ttu-id="d194e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d194e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d194e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d194e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d194e-129">입력</span><span class="sxs-lookup"><span data-stu-id="d194e-129">INPUTS</span></span>

### <span data-ttu-id="d194e-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d194e-130">System.String</span></span>

## <span data-ttu-id="d194e-131">출력</span><span class="sxs-lookup"><span data-stu-id="d194e-131">OUTPUTS</span></span>

### <span data-ttu-id="d194e-132">ServerKeyVaultKey. AzureSqlServerKeyVaultKeyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="d194e-132">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="d194e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d194e-133">NOTES</span></span>

## <span data-ttu-id="d194e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d194e-134">RELATED LINKS</span></span>

[<span data-ttu-id="d194e-135">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d194e-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
