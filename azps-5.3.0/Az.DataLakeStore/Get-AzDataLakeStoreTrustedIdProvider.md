---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489136"
---
# <span data-ttu-id="4f446-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4f446-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="4f446-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f446-102">SYNOPSIS</span></span>
<span data-ttu-id="4f446-103">지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f446-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="4f446-104">공급자를 지정하지 않으면 계정에 대한 모든 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4f446-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="4f446-105">구문</span><span class="sxs-lookup"><span data-stu-id="4f446-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f446-106">설명</span><span class="sxs-lookup"><span data-stu-id="4f446-106">DESCRIPTION</span></span>
<span data-ttu-id="4f446-107">**Get-AzDataLakeStoreTrustedIdProvider** cmdlet은 지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f446-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="4f446-108">공급자를 지정하지 않으면 계정에 대한 모든 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4f446-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="4f446-109">예제</span><span class="sxs-lookup"><span data-stu-id="4f446-109">EXAMPLES</span></span>

### <span data-ttu-id="4f446-110">예제 1: 신뢰할 수 있는 특정 ID 공급자를 얻게</span><span class="sxs-lookup"><span data-stu-id="4f446-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="4f446-111">계정 "ContosoADL"에서 "MyProvider"라는 공급자를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4f446-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="4f446-112">예제 2: 계정의 모든 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="4f446-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="4f446-113">"ContosoADL" 계정의 모든 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4f446-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="4f446-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f446-114">PARAMETERS</span></span>

### <span data-ttu-id="4f446-115">-Account</span><span class="sxs-lookup"><span data-stu-id="4f446-115">-Account</span></span>
<span data-ttu-id="4f446-116">신뢰할 수 있는 ID 공급자를 검색할 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="4f446-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="4f446-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f446-117">-DefaultProfile</span></span>
<span data-ttu-id="4f446-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4f446-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f446-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4f446-119">-Name</span></span>
<span data-ttu-id="4f446-120">검색할 신뢰할 수 있는 ID 공급자의 이름</span><span class="sxs-lookup"><span data-stu-id="4f446-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="4f446-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f446-121">-ResourceGroupName</span></span>
<span data-ttu-id="4f446-122">지정된 계정의 신뢰할 수 있는 ID 공급자를 검색하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f446-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="4f446-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f446-123">CommonParameters</span></span>
<span data-ttu-id="4f446-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f446-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f446-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4f446-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f446-126">입력</span><span class="sxs-lookup"><span data-stu-id="4f446-126">INPUTS</span></span>

### <span data-ttu-id="4f446-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4f446-127">System.String</span></span>

## <span data-ttu-id="4f446-128">출력</span><span class="sxs-lookup"><span data-stu-id="4f446-128">OUTPUTS</span></span>

### <span data-ttu-id="4f446-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4f446-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="4f446-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f446-130">NOTES</span></span>

## <span data-ttu-id="4f446-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f446-131">RELATED LINKS</span></span>
