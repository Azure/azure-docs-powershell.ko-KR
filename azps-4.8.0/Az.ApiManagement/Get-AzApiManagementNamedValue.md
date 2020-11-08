---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048019"
---
# <span data-ttu-id="78424-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="78424-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="78424-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78424-102">SYNOPSIS</span></span>
<span data-ttu-id="78424-103">목록 또는 특정 명명 된 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78424-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="78424-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78424-104">SYNTAX</span></span>

### <span data-ttu-id="78424-105">GetAllNamedValues (기본값)</span><span class="sxs-lookup"><span data-stu-id="78424-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78424-106">Getbynamedeid</span><span class="sxs-lookup"><span data-stu-id="78424-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78424-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="78424-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78424-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="78424-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78424-109">설명은</span><span class="sxs-lookup"><span data-stu-id="78424-109">DESCRIPTION</span></span>
<span data-ttu-id="78424-110">**AzApiManagementNamedValue** cmdlet은 목록 또는 특정 명명 된 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78424-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="78424-111">값은 암호로 표시 된 명명 된 값에는 결과 세부 정보에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78424-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="78424-112">비밀 값을 가져오려면 Get-help를 **AzApiManagementNamedValueSecretValue** 를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="78424-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="78424-113">예제의</span><span class="sxs-lookup"><span data-stu-id="78424-113">EXAMPLES</span></span>

### <span data-ttu-id="78424-114">예제 1: 이름으로 명명 된 값 가져오기</span><span class="sxs-lookup"><span data-stu-id="78424-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="78424-115">이 명령은 명명 된 값 이름이 지정 된 명명 된 값 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78424-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="78424-116">변수</span><span class="sxs-lookup"><span data-stu-id="78424-116">PARAMETERS</span></span>

### <span data-ttu-id="78424-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="78424-117">-Context</span></span>
<span data-ttu-id="78424-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="78424-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="78424-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="78424-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78424-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78424-120">-DefaultProfile</span></span>
<span data-ttu-id="78424-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78424-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78424-122">-이름</span><span class="sxs-lookup"><span data-stu-id="78424-122">-Name</span></span>
<span data-ttu-id="78424-123">문자열 이름을 포함 하는 이름으로 명명 된 값을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="78424-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="78424-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="78424-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78424-125">-Named= Eid</span><span class="sxs-lookup"><span data-stu-id="78424-125">-NamedValueId</span></span>
<span data-ttu-id="78424-126">명명 된 값의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="78424-126">Identifier of the named value.</span></span>
<span data-ttu-id="78424-127">지정 된 경우 식별자를 사용 하 여 명명 된 값을 찾으려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="78424-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="78424-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="78424-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78424-129">태그</span><span class="sxs-lookup"><span data-stu-id="78424-129">-Tag</span></span>
<span data-ttu-id="78424-130">태그와 연관 된 명명 된 값을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="78424-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="78424-131">지정 된 경우 태그와 연결 된 모든 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78424-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="78424-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="78424-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78424-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78424-133">CommonParameters</span></span>
<span data-ttu-id="78424-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78424-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78424-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="78424-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78424-136">입력</span><span class="sxs-lookup"><span data-stu-id="78424-136">INPUTS</span></span>

### <span data-ttu-id="78424-137">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="78424-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="78424-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78424-138">System.String</span></span>

## <span data-ttu-id="78424-139">출력</span><span class="sxs-lookup"><span data-stu-id="78424-139">OUTPUTS</span></span>

### <span data-ttu-id="78424-140">ApiManagement. ServiceManagement. \ PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="78424-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="78424-141">상속자</span><span class="sxs-lookup"><span data-stu-id="78424-141">NOTES</span></span>

## <span data-ttu-id="78424-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78424-142">RELATED LINKS</span></span>
