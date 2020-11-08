---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041957"
---
# <span data-ttu-id="f9b4e-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9b4e-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="f9b4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b4e-103">목록 또는 특정 API 관리 서비스 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="f9b4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9b4e-104">SYNTAX</span></span>

### <span data-ttu-id="f9b4e-105">GetBySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="f9b4e-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9b4e-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9b4e-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9b4e-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="f9b4e-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9b4e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9b4e-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9b4e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f9b4e-109">DESCRIPTION</span></span>
<span data-ttu-id="f9b4e-110">**AzApiManagement** cmdlet은 구독 또는 지정 된 리소스 그룹 또는 특정 API management 아래에 있는 모든 API management 서비스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="f9b4e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f9b4e-111">EXAMPLES</span></span>

### <span data-ttu-id="f9b4e-112">예제 1: 모든 API Management 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="f9b4e-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="f9b4e-113">이 명령은 구독 내의 모든 API Management 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="f9b4e-114">예제 2: 모든 API Management 서비스를 특정 이름으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="f9b4e-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="f9b4e-115">이 명령은 모든 API Management 서비스를 이름별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="f9b4e-116">변수</span><span class="sxs-lookup"><span data-stu-id="f9b4e-116">PARAMETERS</span></span>

### <span data-ttu-id="f9b4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b4e-117">-DefaultProfile</span></span>
<span data-ttu-id="f9b4e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9b4e-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f9b4e-119">-Name</span></span>
<span data-ttu-id="f9b4e-120">API Management 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="f9b4e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b4e-121">-ResourceGroupName</span></span>
<span data-ttu-id="f9b4e-122">이 cmdlet가 API Management 서비스를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="f9b4e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9b4e-123">-ResourceId</span></span>
<span data-ttu-id="f9b4e-124">API Management 서비스의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b4e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b4e-125">CommonParameters</span></span>
<span data-ttu-id="f9b4e-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b4e-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b4e-128">입력</span><span class="sxs-lookup"><span data-stu-id="f9b4e-128">INPUTS</span></span>

### <span data-ttu-id="f9b4e-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f9b4e-129">System.String</span></span>

## <span data-ttu-id="f9b4e-130">출력</span><span class="sxs-lookup"><span data-stu-id="f9b4e-130">OUTPUTS</span></span>

### <span data-ttu-id="f9b4e-131">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="f9b4e-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f9b4e-132">상속자</span><span class="sxs-lookup"><span data-stu-id="f9b4e-132">NOTES</span></span>

## <span data-ttu-id="f9b4e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9b4e-133">RELATED LINKS</span></span>

[<span data-ttu-id="f9b4e-134">백업-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9b4e-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="f9b4e-135">새로운 AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9b4e-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="f9b4e-136">제거-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9b4e-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="f9b4e-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9b4e-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


