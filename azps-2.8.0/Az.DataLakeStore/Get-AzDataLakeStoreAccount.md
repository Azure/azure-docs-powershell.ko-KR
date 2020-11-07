---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: b06b64b81679d1f0f9429be0362f936046e54ee5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696861"
---
# <span data-ttu-id="311b0-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="311b0-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="311b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="311b0-102">SYNOPSIS</span></span>
<span data-ttu-id="311b0-103">Data Lake Store 계정의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="311b0-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="311b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="311b0-104">SYNTAX</span></span>

### <span data-ttu-id="311b0-105">GetAllInSubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="311b0-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="311b0-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="311b0-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="311b0-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="311b0-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="311b0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="311b0-108">DESCRIPTION</span></span>
<span data-ttu-id="311b0-109">**AzDataLakeStoreAccount** Cmdlet은 Data Lake store 계정에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="311b0-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="311b0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="311b0-110">EXAMPLES</span></span>

### <span data-ttu-id="311b0-111">예제 1: Data Lake Store 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="311b0-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="311b0-112">이 명령은 ContosoADL 라는 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="311b0-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="311b0-113">변수</span><span class="sxs-lookup"><span data-stu-id="311b0-113">PARAMETERS</span></span>

### <span data-ttu-id="311b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311b0-114">-DefaultProfile</span></span>
<span data-ttu-id="311b0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="311b0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="311b0-116">-이름</span><span class="sxs-lookup"><span data-stu-id="311b0-116">-Name</span></span>
<span data-ttu-id="311b0-117">가져올 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="311b0-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="311b0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="311b0-118">-ResourceGroupName</span></span>
<span data-ttu-id="311b0-119">가져올 Data Lake Store 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="311b0-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="311b0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311b0-120">CommonParameters</span></span>
<span data-ttu-id="311b0-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="311b0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311b0-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="311b0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311b0-123">입력</span><span class="sxs-lookup"><span data-stu-id="311b0-123">INPUTS</span></span>

### <span data-ttu-id="311b0-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="311b0-124">System.String</span></span>

## <span data-ttu-id="311b0-125">출력</span><span class="sxs-lookup"><span data-stu-id="311b0-125">OUTPUTS</span></span>

### <span data-ttu-id="311b0-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="311b0-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="311b0-127">상속자</span><span class="sxs-lookup"><span data-stu-id="311b0-127">NOTES</span></span>

## <span data-ttu-id="311b0-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="311b0-128">RELATED LINKS</span></span>

[<span data-ttu-id="311b0-129">새로운 AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="311b0-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="311b0-130">제거-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="311b0-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="311b0-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="311b0-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="311b0-132">테스트-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="311b0-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


