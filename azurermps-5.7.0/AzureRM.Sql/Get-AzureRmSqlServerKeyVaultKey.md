---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 4f26955db9d99871cb0c5ae127b5977deedacf08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524839"
---
# <span data-ttu-id="899b7-101">Get-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="899b7-101">Get-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="899b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="899b7-102">SYNOPSIS</span></span>
<span data-ttu-id="899b7-103">SQL server의 키 보관소 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-103">Gets a SQL server's Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="899b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="899b7-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="899b7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="899b7-105">DESCRIPTION</span></span>
<span data-ttu-id="899b7-106">Get-AzureRmSqlServerKeyVaultKey cmdlet은 SQL server의 키 자격 증명 모음 키에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-106">The Get-AzureRmSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="899b7-107">KeyId를 제공 하 여 서버의 모든 키를 보거나 특정 키를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="899b7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="899b7-108">EXAMPLES</span></span>

### <span data-ttu-id="899b7-109">예제 1: 모든 키 자격 증명 모음 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="899b7-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzureRmSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="899b7-110">이 명령은 SQL server의 모든 키 자격 증명 모음 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-110">This command gets all the Key Vault keys on a SQL server.</span></span>

<span data-ttu-id="899b7-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지문: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="899b7-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

<span data-ttu-id="899b7-112">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey2_01234567890123456789012345678901 Type: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 지문: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="899b7-112">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="899b7-113">예제 2: 특정 키 보관소 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="899b7-113">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="899b7-114">이 명령은 Id가 ' ' 인 키 보관소 키를 가져온 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 다음 $MyServerKeyVaultKey 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-114">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="899b7-115">$MyServerKeyVaultKey의 속성을 검사 하 여 키 자격 증명 모음에 대 한 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-115">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="899b7-116">변수</span><span class="sxs-lookup"><span data-stu-id="899b7-116">PARAMETERS</span></span>

### <span data-ttu-id="899b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899b7-117">-DefaultProfile</span></span>
<span data-ttu-id="899b7-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="899b7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899b7-119">-KeyId</span><span class="sxs-lookup"><span data-stu-id="899b7-119">-KeyId</span></span>
<span data-ttu-id="899b7-120">Azure 키 자격 증명 모음 KeyId.</span><span class="sxs-lookup"><span data-stu-id="899b7-120">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="899b7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="899b7-121">-ResourceGroupName</span></span>
<span data-ttu-id="899b7-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-122">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="899b7-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="899b7-123">-ServerName</span></span>
<span data-ttu-id="899b7-124">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-124">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="899b7-125">-확인</span><span class="sxs-lookup"><span data-stu-id="899b7-125">-Confirm</span></span>
<span data-ttu-id="899b7-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899b7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="899b7-127">-WhatIf</span></span>
<span data-ttu-id="899b7-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="899b7-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899b7-130">CommonParameters</span></span>
<span data-ttu-id="899b7-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="899b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899b7-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="899b7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899b7-133">입력</span><span class="sxs-lookup"><span data-stu-id="899b7-133">INPUTS</span></span>

### <span data-ttu-id="899b7-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="899b7-134">System.String</span></span>

## <span data-ttu-id="899b7-135">출력</span><span class="sxs-lookup"><span data-stu-id="899b7-135">OUTPUTS</span></span>

### <span data-ttu-id="899b7-136">System. 개체</span><span class="sxs-lookup"><span data-stu-id="899b7-136">System.Object</span></span>

## <span data-ttu-id="899b7-137">상속자</span><span class="sxs-lookup"><span data-stu-id="899b7-137">NOTES</span></span>

## <span data-ttu-id="899b7-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="899b7-138">RELATED LINKS</span></span>

[<span data-ttu-id="899b7-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="899b7-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
