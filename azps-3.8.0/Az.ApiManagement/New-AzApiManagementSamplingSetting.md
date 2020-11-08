---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 61f046576c14b61a59b55c52dd69c3e72b2c839e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042217"
---
# <span data-ttu-id="5dafe-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5dafe-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="5dafe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dafe-102">SYNOPSIS</span></span>
<span data-ttu-id="5dafe-103">진단에 대 한 새 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="5dafe-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="5dafe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5dafe-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dafe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5dafe-105">DESCRIPTION</span></span>
<span data-ttu-id="5dafe-106">Cmdlet **AzApiManagementSamplingSetting** 는 진단에 대 한 새 샘플링 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5dafe-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="5dafe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5dafe-107">EXAMPLES</span></span>

### <span data-ttu-id="5dafe-108">예제 1: 기본 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="5dafe-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="5dafe-109">`Fixed`요청/응답의 100%에 대 한 로깅을 사용 하 여 유형의 샘플링 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5dafe-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="5dafe-110">변수</span><span class="sxs-lookup"><span data-stu-id="5dafe-110">PARAMETERS</span></span>

### <span data-ttu-id="5dafe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dafe-111">-DefaultProfile</span></span>
<span data-ttu-id="5dafe-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5dafe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dafe-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="5dafe-113">-SamplingPercentage</span></span>
<span data-ttu-id="5dafe-114">고정 요금 샘플링에 대 한 샘플링 비율입니다.</span><span class="sxs-lookup"><span data-stu-id="5dafe-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="5dafe-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5dafe-115">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dafe-116">-SamplingType</span><span class="sxs-lookup"><span data-stu-id="5dafe-116">-SamplingType</span></span>
<span data-ttu-id="5dafe-117">표본 집단의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5dafe-117">The Type of Sampling.</span></span>
<span data-ttu-id="5dafe-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5dafe-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dafe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dafe-119">CommonParameters</span></span>
<span data-ttu-id="5dafe-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dafe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dafe-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5dafe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dafe-122">입력</span><span class="sxs-lookup"><span data-stu-id="5dafe-122">INPUTS</span></span>

### <span data-ttu-id="5dafe-123">않아야</span><span class="sxs-lookup"><span data-stu-id="5dafe-123">None</span></span>

## <span data-ttu-id="5dafe-124">출력</span><span class="sxs-lookup"><span data-stu-id="5dafe-124">OUTPUTS</span></span>

### <span data-ttu-id="5dafe-125">ApiManagement. ServiceManagement. \ PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5dafe-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="5dafe-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5dafe-126">NOTES</span></span>

## <span data-ttu-id="5dafe-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dafe-127">RELATED LINKS</span></span>

[<span data-ttu-id="5dafe-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5dafe-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="5dafe-129">제거-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5dafe-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="5dafe-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5dafe-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="5dafe-131">새로운 AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5dafe-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
