---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 61899a50c857fc3e8852d362d5905b0ca2fedf6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531733"
---
# <span data-ttu-id="6bbae-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6bbae-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="6bbae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bbae-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbae-103">Data Lake Store 계정의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6bbae-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bbae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6bbae-104">SYNTAX</span></span>

### <span data-ttu-id="6bbae-105">GetAllInSubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="6bbae-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bbae-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6bbae-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6bbae-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="6bbae-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bbae-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6bbae-108">DESCRIPTION</span></span>
<span data-ttu-id="6bbae-109">**AzureRmDataLakeStoreAccount** Cmdlet은 Data Lake store 계정에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6bbae-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="6bbae-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6bbae-110">EXAMPLES</span></span>

### <span data-ttu-id="6bbae-111">예제 1: Data Lake Store 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="6bbae-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="6bbae-112">이 명령은 ContosoADL 라는 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6bbae-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="6bbae-113">변수</span><span class="sxs-lookup"><span data-stu-id="6bbae-113">PARAMETERS</span></span>

### <span data-ttu-id="6bbae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbae-114">-DefaultProfile</span></span>
<span data-ttu-id="6bbae-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6bbae-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bbae-116">-이름</span><span class="sxs-lookup"><span data-stu-id="6bbae-116">-Name</span></span>
<span data-ttu-id="6bbae-117">가져올 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bbae-117">Specifies the name of the account to get.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbae-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bbae-118">-ResourceGroupName</span></span>
<span data-ttu-id="6bbae-119">가져올 Data Lake Store 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bbae-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbae-120">CommonParameters</span></span>
<span data-ttu-id="6bbae-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bbae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbae-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bbae-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbae-123">입력</span><span class="sxs-lookup"><span data-stu-id="6bbae-123">INPUTS</span></span>

### <span data-ttu-id="6bbae-124">않아야</span><span class="sxs-lookup"><span data-stu-id="6bbae-124">None</span></span>
<span data-ttu-id="6bbae-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6bbae-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6bbae-126">출력</span><span class="sxs-lookup"><span data-stu-id="6bbae-126">OUTPUTS</span></span>

### <span data-ttu-id="6bbae-127">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6bbae-127">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="6bbae-128">요청한 특정 Data Lake Store 계정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bbae-128">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="6bbae-129">목록<PSDataLakeStoreAccountBasic></span><span class="sxs-lookup"><span data-stu-id="6bbae-129">List<PSDataLakeStoreAccountBasic></span></span>
<span data-ttu-id="6bbae-130">지정 된 리소스 그룹 또는 구독의 Data Lake Store 계정 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6bbae-130">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="6bbae-131">상속자</span><span class="sxs-lookup"><span data-stu-id="6bbae-131">NOTES</span></span>

## <span data-ttu-id="6bbae-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bbae-132">RELATED LINKS</span></span>

[<span data-ttu-id="6bbae-133">새로운 AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6bbae-133">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6bbae-134">제거-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6bbae-134">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6bbae-135">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6bbae-135">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6bbae-136">테스트-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6bbae-136">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


