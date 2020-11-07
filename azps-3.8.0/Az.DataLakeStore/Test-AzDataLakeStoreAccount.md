---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879850"
---
# <span data-ttu-id="e0a3f-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e0a3f-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="e0a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a3f-103">Data Lake Store 계정이 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3f-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="e0a3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0a3f-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0a3f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e0a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="e0a3f-106">**테스트 AzDataLakeStoreAccount** Cmdlet은 Data Lake store 계정이 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3f-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="e0a3f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e0a3f-107">EXAMPLES</span></span>

### <span data-ttu-id="e0a3f-108">예제 1: 계정 테스트</span><span class="sxs-lookup"><span data-stu-id="e0a3f-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="e0a3f-109">이 명령은 ContosoADL 이라는 계정이 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3f-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="e0a3f-110">변수</span><span class="sxs-lookup"><span data-stu-id="e0a3f-110">PARAMETERS</span></span>

### <span data-ttu-id="e0a3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a3f-111">-DefaultProfile</span></span>
<span data-ttu-id="e0a3f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e0a3f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0a3f-113">-이름</span><span class="sxs-lookup"><span data-stu-id="e0a3f-113">-Name</span></span>
<span data-ttu-id="e0a3f-114">테스트할 Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3f-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="e0a3f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a3f-115">-ResourceGroupName</span></span>
<span data-ttu-id="e0a3f-116">테스트할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3f-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="e0a3f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a3f-117">CommonParameters</span></span>
<span data-ttu-id="e0a3f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a3f-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0a3f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a3f-120">입력</span><span class="sxs-lookup"><span data-stu-id="e0a3f-120">INPUTS</span></span>

### <span data-ttu-id="e0a3f-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e0a3f-121">System.String</span></span>

## <span data-ttu-id="e0a3f-122">출력</span><span class="sxs-lookup"><span data-stu-id="e0a3f-122">OUTPUTS</span></span>

### <span data-ttu-id="e0a3f-123">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e0a3f-123">System.Boolean</span></span>

## <span data-ttu-id="e0a3f-124">상속자</span><span class="sxs-lookup"><span data-stu-id="e0a3f-124">NOTES</span></span>

## <span data-ttu-id="e0a3f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0a3f-125">RELATED LINKS</span></span>

[<span data-ttu-id="e0a3f-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e0a3f-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e0a3f-127">새로운 AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e0a3f-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e0a3f-128">제거-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e0a3f-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e0a3f-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e0a3f-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


