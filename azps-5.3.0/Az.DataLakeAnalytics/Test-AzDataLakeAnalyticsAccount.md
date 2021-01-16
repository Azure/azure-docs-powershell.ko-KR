---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 0f0cad155cdb274596aba449e26e82b94ca56aae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493479"
---
# <span data-ttu-id="d63f2-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d63f2-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d63f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d63f2-102">SYNOPSIS</span></span>
<span data-ttu-id="d63f2-103">Data Lake Analytics 계정의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d63f2-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d63f2-104">구문</span><span class="sxs-lookup"><span data-stu-id="d63f2-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d63f2-105">설명</span><span class="sxs-lookup"><span data-stu-id="d63f2-105">DESCRIPTION</span></span>
<span data-ttu-id="d63f2-106">**Test-AzDataLakeAnalyticsAccount** cmdlet은 Data Lake Analytics 계정의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d63f2-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d63f2-107">예제</span><span class="sxs-lookup"><span data-stu-id="d63f2-107">EXAMPLES</span></span>

### <span data-ttu-id="d63f2-108">예제 1: 계정이 있는지 여부 테스트</span><span class="sxs-lookup"><span data-stu-id="d63f2-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="d63f2-109">이 명령은 ContosoAdlAccount라는 계정이 있는지 여부를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="d63f2-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="d63f2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d63f2-110">PARAMETERS</span></span>

### <span data-ttu-id="d63f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d63f2-111">-DefaultProfile</span></span>
<span data-ttu-id="d63f2-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d63f2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d63f2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d63f2-113">-Name</span></span>
<span data-ttu-id="d63f2-114">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d63f2-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d63f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d63f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="d63f2-116">Data Lake Analytics 계정의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d63f2-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="d63f2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d63f2-117">CommonParameters</span></span>
<span data-ttu-id="d63f2-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d63f2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d63f2-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d63f2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d63f2-120">입력</span><span class="sxs-lookup"><span data-stu-id="d63f2-120">INPUTS</span></span>

### <span data-ttu-id="d63f2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d63f2-121">System.String</span></span>

## <span data-ttu-id="d63f2-122">출력</span><span class="sxs-lookup"><span data-stu-id="d63f2-122">OUTPUTS</span></span>

### <span data-ttu-id="d63f2-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d63f2-123">System.Boolean</span></span>

## <span data-ttu-id="d63f2-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d63f2-124">NOTES</span></span>

## <span data-ttu-id="d63f2-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d63f2-125">RELATED LINKS</span></span>

[<span data-ttu-id="d63f2-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d63f2-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d63f2-127">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d63f2-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d63f2-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d63f2-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


