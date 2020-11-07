---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878362"
---
# <span data-ttu-id="50b4e-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="50b4e-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="50b4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="50b4e-103">지정한 Data Lake Store에서 지정 된 신뢰할 수 있는 id 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50b4e-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="50b4e-104">공급자가 지정 되지 않은 경우 계정에 대 한 모든 공급자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50b4e-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="50b4e-105">구문과</span><span class="sxs-lookup"><span data-stu-id="50b4e-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50b4e-106">설명은</span><span class="sxs-lookup"><span data-stu-id="50b4e-106">DESCRIPTION</span></span>
<span data-ttu-id="50b4e-107">**AzDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store에서 지정 된 신뢰할 수 있는 id 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50b4e-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="50b4e-108">공급자가 지정 되지 않은 경우 계정에 대 한 모든 공급자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50b4e-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="50b4e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="50b4e-109">EXAMPLES</span></span>

### <span data-ttu-id="50b4e-110">예제 1: 신뢰할 수 있는 특정 id 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="50b4e-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="50b4e-111">"ContosoADL" 계정의 "MyProvider" 공급자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="50b4e-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="50b4e-112">예제 2: 계정의 모든 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="50b4e-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="50b4e-113">계정 "ContosoADL"의 모든 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="50b4e-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="50b4e-114">변수</span><span class="sxs-lookup"><span data-stu-id="50b4e-114">PARAMETERS</span></span>

### <span data-ttu-id="50b4e-115">-계정</span><span class="sxs-lookup"><span data-stu-id="50b4e-115">-Account</span></span>
<span data-ttu-id="50b4e-116">신뢰할 수 있는 id 공급자를 검색 하기 위한 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="50b4e-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="50b4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b4e-117">-DefaultProfile</span></span>
<span data-ttu-id="50b4e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="50b4e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50b4e-119">-이름</span><span class="sxs-lookup"><span data-stu-id="50b4e-119">-Name</span></span>
<span data-ttu-id="50b4e-120">검색할 신뢰할 수 있는 id 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50b4e-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="50b4e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50b4e-121">-ResourceGroupName</span></span>
<span data-ttu-id="50b4e-122">지정 된 계정의 신뢰할 수 있는 id 공급자를 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50b4e-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="50b4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b4e-123">CommonParameters</span></span>
<span data-ttu-id="50b4e-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50b4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b4e-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50b4e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b4e-126">입력</span><span class="sxs-lookup"><span data-stu-id="50b4e-126">INPUTS</span></span>

### <span data-ttu-id="50b4e-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="50b4e-127">System.String</span></span>

## <span data-ttu-id="50b4e-128">출력</span><span class="sxs-lookup"><span data-stu-id="50b4e-128">OUTPUTS</span></span>

### <span data-ttu-id="50b4e-129">DataLakeStore. DataLakeStoreTrustedIdProvider/.</span><span class="sxs-lookup"><span data-stu-id="50b4e-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="50b4e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="50b4e-130">NOTES</span></span>

## <span data-ttu-id="50b4e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50b4e-131">RELATED LINKS</span></span>
