---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 77247853fe6412b0d01fb01c71e592efca12063d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868578"
---
# <span data-ttu-id="c80a3-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c80a3-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="c80a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c80a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c80a3-103">Data Lake Analytics 계정이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c80a3-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="c80a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c80a3-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c80a3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c80a3-105">DESCRIPTION</span></span>
<span data-ttu-id="c80a3-106">**AzDataLakeAnalyticsAccount** Cmdlet은 Data Lake Analytics 계정이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c80a3-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="c80a3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c80a3-107">EXAMPLES</span></span>

### <span data-ttu-id="c80a3-108">예제 1: 계정이 있는지 테스트</span><span class="sxs-lookup"><span data-stu-id="c80a3-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="c80a3-109">이 명령은 ContosoAdlAccount 이라는 계정이 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c80a3-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="c80a3-110">변수</span><span class="sxs-lookup"><span data-stu-id="c80a3-110">PARAMETERS</span></span>

### <span data-ttu-id="c80a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80a3-111">-DefaultProfile</span></span>
<span data-ttu-id="c80a3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c80a3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c80a3-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c80a3-113">-Name</span></span>
<span data-ttu-id="c80a3-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c80a3-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c80a3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c80a3-115">-ResourceGroupName</span></span>
<span data-ttu-id="c80a3-116">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c80a3-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="c80a3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80a3-117">CommonParameters</span></span>
<span data-ttu-id="c80a3-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c80a3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80a3-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c80a3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80a3-120">입력</span><span class="sxs-lookup"><span data-stu-id="c80a3-120">INPUTS</span></span>

### <span data-ttu-id="c80a3-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c80a3-121">System.String</span></span>

## <span data-ttu-id="c80a3-122">출력</span><span class="sxs-lookup"><span data-stu-id="c80a3-122">OUTPUTS</span></span>

### <span data-ttu-id="c80a3-123">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c80a3-123">System.Boolean</span></span>

## <span data-ttu-id="c80a3-124">상속자</span><span class="sxs-lookup"><span data-stu-id="c80a3-124">NOTES</span></span>

## <span data-ttu-id="c80a3-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c80a3-125">RELATED LINKS</span></span>

[<span data-ttu-id="c80a3-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c80a3-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c80a3-127">새로운 AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c80a3-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c80a3-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c80a3-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


