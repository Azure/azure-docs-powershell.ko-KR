---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b1b3a05b6f2d19ba350567c8793822d4129c5445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93701972"
---
# <span data-ttu-id="7e6fc-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7e6fc-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="7e6fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="7e6fc-103">Data Lake Store 계정이 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6fc-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e6fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e6fc-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e6fc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7e6fc-105">DESCRIPTION</span></span>
<span data-ttu-id="7e6fc-106">**테스트 AzureRmDataLakeStoreAccount** Cmdlet은 Data Lake store 계정이 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6fc-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="7e6fc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7e6fc-107">EXAMPLES</span></span>

### <span data-ttu-id="7e6fc-108">예제 1: 계정 테스트</span><span class="sxs-lookup"><span data-stu-id="7e6fc-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="7e6fc-109">이 명령은 ContosoADL 이라는 계정이 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6fc-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="7e6fc-110">변수</span><span class="sxs-lookup"><span data-stu-id="7e6fc-110">PARAMETERS</span></span>

### <span data-ttu-id="7e6fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e6fc-111">-DefaultProfile</span></span>
<span data-ttu-id="7e6fc-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7e6fc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e6fc-113">-이름</span><span class="sxs-lookup"><span data-stu-id="7e6fc-113">-Name</span></span>
<span data-ttu-id="7e6fc-114">테스트할 Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6fc-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="7e6fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e6fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="7e6fc-116">테스트할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6fc-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="7e6fc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e6fc-117">CommonParameters</span></span>
<span data-ttu-id="7e6fc-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6fc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e6fc-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e6fc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e6fc-120">입력</span><span class="sxs-lookup"><span data-stu-id="7e6fc-120">INPUTS</span></span>

### <span data-ttu-id="7e6fc-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e6fc-121">System.String</span></span>

## <span data-ttu-id="7e6fc-122">출력</span><span class="sxs-lookup"><span data-stu-id="7e6fc-122">OUTPUTS</span></span>

### <span data-ttu-id="7e6fc-123">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7e6fc-123">System.Boolean</span></span>

## <span data-ttu-id="7e6fc-124">상속자</span><span class="sxs-lookup"><span data-stu-id="7e6fc-124">NOTES</span></span>

## <span data-ttu-id="7e6fc-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e6fc-125">RELATED LINKS</span></span>

[<span data-ttu-id="7e6fc-126">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7e6fc-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7e6fc-127">새로운 AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7e6fc-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7e6fc-128">제거-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7e6fc-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7e6fc-129">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7e6fc-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


