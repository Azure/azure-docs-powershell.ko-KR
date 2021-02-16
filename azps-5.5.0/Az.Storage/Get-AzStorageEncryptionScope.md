---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: cdc2f8b1742625feb042865a9b75e2c495d7aac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178201"
---
# <span data-ttu-id="c9a0a-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="c9a0a-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="c9a0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a0a-103">Storage 계정에서 암호화 범위를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="c9a0a-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9a0a-104">SYNTAX</span></span>

### <span data-ttu-id="c9a0a-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c9a0a-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9a0a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c9a0a-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9a0a-107">설명</span><span class="sxs-lookup"><span data-stu-id="c9a0a-107">DESCRIPTION</span></span>
<span data-ttu-id="c9a0a-108">**Get-AzStorageEncryptionScope** cmdlet은 Storage 계정에서 암호화 범위를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="c9a0a-109">예제</span><span class="sxs-lookup"><span data-stu-id="c9a0a-109">EXAMPLES</span></span>

### <span data-ttu-id="c9a0a-110">예제 1: 단일 암호화 범위 얻기</span><span class="sxs-lookup"><span data-stu-id="c9a0a-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="c9a0a-111">이 명령은 단일 암호화 범위를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="c9a0a-112">예제 2: Storage 계정의 모든 암호화 범위 나열</span><span class="sxs-lookup"><span data-stu-id="c9a0a-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="c9a0a-113">이 명령은 Storage 계정의 모든 암호화 범위를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="c9a0a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9a0a-114">PARAMETERS</span></span>

### <span data-ttu-id="c9a0a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a0a-115">-DefaultProfile</span></span>
<span data-ttu-id="c9a0a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9a0a-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="c9a0a-117">-EncryptionScopeName</span></span>
<span data-ttu-id="c9a0a-118">Azure Storage EncryptionScope 이름</span><span class="sxs-lookup"><span data-stu-id="c9a0a-118">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9a0a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a0a-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9a0a-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9a0a-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9a0a-121">-StorageAccount</span></span>
<span data-ttu-id="c9a0a-122">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="c9a0a-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9a0a-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c9a0a-123">-StorageAccountName</span></span>
<span data-ttu-id="c9a0a-124">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9a0a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a0a-125">CommonParameters</span></span>
<span data-ttu-id="c9a0a-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a0a-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9a0a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a0a-128">입력</span><span class="sxs-lookup"><span data-stu-id="c9a0a-128">INPUTS</span></span>

### <span data-ttu-id="c9a0a-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9a0a-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c9a0a-130">출력</span><span class="sxs-lookup"><span data-stu-id="c9a0a-130">OUTPUTS</span></span>

### <span data-ttu-id="c9a0a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="c9a0a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="c9a0a-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9a0a-132">NOTES</span></span>

## <span data-ttu-id="c9a0a-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9a0a-133">RELATED LINKS</span></span>
