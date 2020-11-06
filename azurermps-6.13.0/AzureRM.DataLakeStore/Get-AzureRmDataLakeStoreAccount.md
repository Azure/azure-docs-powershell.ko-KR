---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f15ef7201622394a2b96964244980b059f1222c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524472"
---
# <span data-ttu-id="035d5-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035d5-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="035d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="035d5-102">SYNOPSIS</span></span>
<span data-ttu-id="035d5-103">Data Lake Store 계정의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="035d5-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="035d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="035d5-104">SYNTAX</span></span>

### <span data-ttu-id="035d5-105">GetAllInSubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="035d5-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="035d5-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="035d5-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="035d5-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="035d5-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="035d5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="035d5-108">DESCRIPTION</span></span>
<span data-ttu-id="035d5-109">**AzureRmDataLakeStoreAccount** Cmdlet은 Data Lake store 계정에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="035d5-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="035d5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="035d5-110">EXAMPLES</span></span>

### <span data-ttu-id="035d5-111">예제 1: Data Lake Store 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="035d5-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="035d5-112">이 명령은 ContosoADL 라는 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="035d5-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="035d5-113">변수</span><span class="sxs-lookup"><span data-stu-id="035d5-113">PARAMETERS</span></span>

### <span data-ttu-id="035d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035d5-114">-DefaultProfile</span></span>
<span data-ttu-id="035d5-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="035d5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="035d5-116">-이름</span><span class="sxs-lookup"><span data-stu-id="035d5-116">-Name</span></span>
<span data-ttu-id="035d5-117">가져올 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="035d5-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="035d5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="035d5-118">-ResourceGroupName</span></span>
<span data-ttu-id="035d5-119">가져올 Data Lake Store 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="035d5-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="035d5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035d5-120">CommonParameters</span></span>
<span data-ttu-id="035d5-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="035d5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035d5-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="035d5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035d5-123">입력</span><span class="sxs-lookup"><span data-stu-id="035d5-123">INPUTS</span></span>

### <span data-ttu-id="035d5-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="035d5-124">System.String</span></span>

## <span data-ttu-id="035d5-125">출력</span><span class="sxs-lookup"><span data-stu-id="035d5-125">OUTPUTS</span></span>

### <span data-ttu-id="035d5-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035d5-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="035d5-127">상속자</span><span class="sxs-lookup"><span data-stu-id="035d5-127">NOTES</span></span>

## <span data-ttu-id="035d5-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="035d5-128">RELATED LINKS</span></span>

[<span data-ttu-id="035d5-129">새로운 AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035d5-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="035d5-130">제거-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035d5-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="035d5-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035d5-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="035d5-132">테스트-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035d5-132">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


