---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94055977"
---
# <span data-ttu-id="a473b-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a473b-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="a473b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a473b-102">SYNOPSIS</span></span>
<span data-ttu-id="a473b-103">백 엔드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="a473b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a473b-104">SYNTAX</span></span>

### <span data-ttu-id="a473b-105">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a473b-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a473b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a473b-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a473b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a473b-107">DESCRIPTION</span></span>
<span data-ttu-id="a473b-108">백 엔드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="a473b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a473b-109">EXAMPLES</span></span>

### <span data-ttu-id="a473b-110">예제 1: 모든 백 엔드 가져오기</span><span class="sxs-lookup"><span data-stu-id="a473b-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="a473b-111">Api Management 서비스에 구성 된 모든 Backends의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="a473b-112">예제 2: 식별자 123으로 지정 된 백 엔드 가져오기</span><span class="sxs-lookup"><span data-stu-id="a473b-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="a473b-113">식별자 ' 123 ' (으)로 식별 되는 지정 된 백엔드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="a473b-114">변수</span><span class="sxs-lookup"><span data-stu-id="a473b-114">PARAMETERS</span></span>

### <span data-ttu-id="a473b-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="a473b-115">-BackendId</span></span>
<span data-ttu-id="a473b-116">백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-116">Identifier of a backend.</span></span>
<span data-ttu-id="a473b-117">지정 된 경우 식별자를 사용 하 여 백 엔드를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="a473b-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a473b-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a473b-119">-Context</span></span>
<span data-ttu-id="a473b-120">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a473b-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a473b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a473b-122">-DefaultProfile</span></span>
<span data-ttu-id="a473b-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a473b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a473b-124">-ResourceId</span></span>
<span data-ttu-id="a473b-125">백 엔드의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="a473b-126">지정 된 경우 식별자를 사용 하 여 백 엔드를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="a473b-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a473b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a473b-128">CommonParameters</span></span>
<span data-ttu-id="a473b-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a473b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a473b-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a473b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a473b-131">입력</span><span class="sxs-lookup"><span data-stu-id="a473b-131">INPUTS</span></span>

### <span data-ttu-id="a473b-132">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a473b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a473b-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a473b-133">System.String</span></span>

## <span data-ttu-id="a473b-134">출력</span><span class="sxs-lookup"><span data-stu-id="a473b-134">OUTPUTS</span></span>

### <span data-ttu-id="a473b-135">ApiManagement. ServiceManagement. \ PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a473b-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="a473b-136">상속자</span><span class="sxs-lookup"><span data-stu-id="a473b-136">NOTES</span></span>

## <span data-ttu-id="a473b-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a473b-137">RELATED LINKS</span></span>

[<span data-ttu-id="a473b-138">새로운 AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a473b-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="a473b-139">새로운 AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a473b-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="a473b-140">새로운 AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a473b-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="a473b-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a473b-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="a473b-142">제거-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a473b-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
