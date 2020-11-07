---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 12f0aa4d198a93d1e392aa61294de6e5815196b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698025"
---
# <span data-ttu-id="c7474-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c7474-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="c7474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7474-102">SYNOPSIS</span></span>
<span data-ttu-id="c7474-103">진단에 대 한 새 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="c7474-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="c7474-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7474-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7474-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c7474-105">DESCRIPTION</span></span>
<span data-ttu-id="c7474-106">Cmdlet **AzApiManagementSamplingSetting** 는 진단에 대 한 새 샘플링 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7474-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="c7474-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c7474-107">EXAMPLES</span></span>

### <span data-ttu-id="c7474-108">예제 1: 기본 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="c7474-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="c7474-109">`Fixed`요청/응답의 100%에 대 한 로깅을 사용 하 여 유형의 샘플링 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7474-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="c7474-110">변수</span><span class="sxs-lookup"><span data-stu-id="c7474-110">PARAMETERS</span></span>

### <span data-ttu-id="c7474-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7474-111">-DefaultProfile</span></span>
<span data-ttu-id="c7474-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7474-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7474-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="c7474-113">-SamplingPercentage</span></span>
<span data-ttu-id="c7474-114">고정 요금 샘플링에 대 한 샘플링 비율입니다.</span><span class="sxs-lookup"><span data-stu-id="c7474-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="c7474-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c7474-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7474-116">-SamplingType</span><span class="sxs-lookup"><span data-stu-id="c7474-116">-SamplingType</span></span>
<span data-ttu-id="c7474-117">표본 집단의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c7474-117">The Type of Sampling.</span></span>
<span data-ttu-id="c7474-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c7474-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7474-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7474-119">CommonParameters</span></span>
<span data-ttu-id="c7474-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7474-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7474-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7474-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7474-122">입력</span><span class="sxs-lookup"><span data-stu-id="c7474-122">INPUTS</span></span>

### <span data-ttu-id="c7474-123">않아야</span><span class="sxs-lookup"><span data-stu-id="c7474-123">None</span></span>

## <span data-ttu-id="c7474-124">출력</span><span class="sxs-lookup"><span data-stu-id="c7474-124">OUTPUTS</span></span>

### <span data-ttu-id="c7474-125">ApiManagement. ServiceManagement. \ PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c7474-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="c7474-126">상속자</span><span class="sxs-lookup"><span data-stu-id="c7474-126">NOTES</span></span>

## <span data-ttu-id="c7474-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7474-127">RELATED LINKS</span></span>

[<span data-ttu-id="c7474-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c7474-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c7474-129">제거-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c7474-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c7474-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c7474-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c7474-131">새로운 AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c7474-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
