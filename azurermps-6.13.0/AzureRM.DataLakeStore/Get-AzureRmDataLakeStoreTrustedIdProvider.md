---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 07bcfff4ab8d1e071ed34c9a52e8aa4e98c32946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528528"
---
# <span data-ttu-id="47567-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="47567-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="47567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47567-102">SYNOPSIS</span></span>
<span data-ttu-id="47567-103">지정한 Data Lake Store에서 지정 된 신뢰할 수 있는 id 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47567-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="47567-104">공급자가 지정 되지 않은 경우 계정에 대 한 모든 공급자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47567-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47567-105">구문과</span><span class="sxs-lookup"><span data-stu-id="47567-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47567-106">설명은</span><span class="sxs-lookup"><span data-stu-id="47567-106">DESCRIPTION</span></span>
<span data-ttu-id="47567-107">**AzureRmDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store에서 지정 된 신뢰할 수 있는 id 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47567-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="47567-108">공급자가 지정 되지 않은 경우 계정에 대 한 모든 공급자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47567-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="47567-109">예제의</span><span class="sxs-lookup"><span data-stu-id="47567-109">EXAMPLES</span></span>

### <span data-ttu-id="47567-110">예제 1: 신뢰할 수 있는 특정 id 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="47567-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="47567-111">"ContosoADL" 계정의 "MyProvider" 공급자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="47567-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="47567-112">예제 2: 계정의 모든 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="47567-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="47567-113">계정 "ContosoADL"의 모든 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="47567-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="47567-114">변수</span><span class="sxs-lookup"><span data-stu-id="47567-114">PARAMETERS</span></span>

### <span data-ttu-id="47567-115">-계정</span><span class="sxs-lookup"><span data-stu-id="47567-115">-Account</span></span>
<span data-ttu-id="47567-116">신뢰할 수 있는 id 공급자를 검색 하기 위한 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="47567-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47567-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47567-117">-DefaultProfile</span></span>
<span data-ttu-id="47567-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="47567-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47567-119">-이름</span><span class="sxs-lookup"><span data-stu-id="47567-119">-Name</span></span>
<span data-ttu-id="47567-120">검색할 신뢰할 수 있는 id 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47567-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47567-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47567-121">-ResourceGroupName</span></span>
<span data-ttu-id="47567-122">지정 된 계정의 신뢰할 수 있는 id 공급자를 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47567-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="47567-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47567-123">CommonParameters</span></span>
<span data-ttu-id="47567-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47567-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47567-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47567-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47567-126">입력</span><span class="sxs-lookup"><span data-stu-id="47567-126">INPUTS</span></span>

### <span data-ttu-id="47567-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="47567-127">System.String</span></span>

## <span data-ttu-id="47567-128">출력</span><span class="sxs-lookup"><span data-stu-id="47567-128">OUTPUTS</span></span>

### <span data-ttu-id="47567-129">DataLakeStore. DataLakeStoreTrustedIdProvider/.</span><span class="sxs-lookup"><span data-stu-id="47567-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="47567-130">상속자</span><span class="sxs-lookup"><span data-stu-id="47567-130">NOTES</span></span>

## <span data-ttu-id="47567-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47567-131">RELATED LINKS</span></span>
