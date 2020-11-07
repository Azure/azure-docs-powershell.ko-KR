---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: c636da952c02b4f2b4795cd1703c276a23a8221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689164"
---
# <span data-ttu-id="27677-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="27677-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="27677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27677-102">SYNOPSIS</span></span>
<span data-ttu-id="27677-103">목록 또는 특정 API 관리 서비스 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27677-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="27677-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27677-104">SYNTAX</span></span>

### <span data-ttu-id="27677-105">GetBySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="27677-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27677-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="27677-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27677-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="27677-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27677-108">설명은</span><span class="sxs-lookup"><span data-stu-id="27677-108">DESCRIPTION</span></span>
<span data-ttu-id="27677-109">**AzApiManagement** cmdlet은 구독 또는 지정 된 리소스 그룹 또는 특정 API management 아래에 있는 모든 API management 서비스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27677-109">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="27677-110">예제의</span><span class="sxs-lookup"><span data-stu-id="27677-110">EXAMPLES</span></span>

### <span data-ttu-id="27677-111">예제 1: 모든 API Management 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="27677-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="27677-112">이 명령은 구독 내의 모든 API Management 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27677-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="27677-113">예제 2: 모든 API Management 서비스를 특정 이름으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="27677-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="27677-114">이 명령은 모든 API Management 서비스를 이름별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27677-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="27677-115">변수</span><span class="sxs-lookup"><span data-stu-id="27677-115">PARAMETERS</span></span>

### <span data-ttu-id="27677-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27677-116">-DefaultProfile</span></span>
<span data-ttu-id="27677-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27677-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27677-118">-이름</span><span class="sxs-lookup"><span data-stu-id="27677-118">-Name</span></span>
<span data-ttu-id="27677-119">API Management 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27677-119">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27677-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27677-120">-ResourceGroupName</span></span>
<span data-ttu-id="27677-121">이 cmdlet가 API Management 서비스를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27677-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27677-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27677-122">CommonParameters</span></span>
<span data-ttu-id="27677-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27677-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27677-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27677-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27677-125">입력</span><span class="sxs-lookup"><span data-stu-id="27677-125">INPUTS</span></span>

### <span data-ttu-id="27677-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="27677-126">System.String</span></span>

## <span data-ttu-id="27677-127">출력</span><span class="sxs-lookup"><span data-stu-id="27677-127">OUTPUTS</span></span>

### <span data-ttu-id="27677-128">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="27677-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="27677-129">상속자</span><span class="sxs-lookup"><span data-stu-id="27677-129">NOTES</span></span>

## <span data-ttu-id="27677-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27677-130">RELATED LINKS</span></span>

[<span data-ttu-id="27677-131">백업-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="27677-131">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="27677-132">새로운 AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="27677-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="27677-133">제거-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="27677-133">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="27677-134">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="27677-134">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


