---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349214"
---
# <span data-ttu-id="aa9d0-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="aa9d0-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="aa9d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9d0-103">목록 또는 특정 명명된 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="aa9d0-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa9d0-104">SYNTAX</span></span>

### <span data-ttu-id="aa9d0-105">GetAllNamedValues(기본값)</span><span class="sxs-lookup"><span data-stu-id="aa9d0-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa9d0-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="aa9d0-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa9d0-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="aa9d0-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa9d0-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="aa9d0-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa9d0-109">설명</span><span class="sxs-lookup"><span data-stu-id="aa9d0-109">DESCRIPTION</span></span>
<span data-ttu-id="aa9d0-110">**Get-AzApiManagementNamedValue** cmdlet은 목록 또는 특정 명명된 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="aa9d0-111">명명된 값이 비밀로 표시된 경우 값이 결과 세부 정보에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="aa9d0-112">비밀 값을 얻습니다. **Get-AzApiManagementNamedValueSecretValue를 사용 합니다.**</span><span class="sxs-lookup"><span data-stu-id="aa9d0-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="aa9d0-113">예제</span><span class="sxs-lookup"><span data-stu-id="aa9d0-113">EXAMPLES</span></span>

### <span data-ttu-id="aa9d0-114">예제 1: 이름으로 명명된 값 얻기</span><span class="sxs-lookup"><span data-stu-id="aa9d0-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="aa9d0-115">이 명령은 명명된 값 이름을 지정하는 명명된 값 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="aa9d0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa9d0-116">PARAMETERS</span></span>

### <span data-ttu-id="aa9d0-117">-Context</span><span class="sxs-lookup"><span data-stu-id="aa9d0-117">-Context</span></span>
<span data-ttu-id="aa9d0-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aa9d0-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-119">This parameter is required.</span></span>

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

### <span data-ttu-id="aa9d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa9d0-120">-DefaultProfile</span></span>
<span data-ttu-id="aa9d0-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa9d0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aa9d0-122">-Name</span></span>
<span data-ttu-id="aa9d0-123">이름 문자열이 포함된 이름이 있는 명명된 값을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="aa9d0-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="aa9d0-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="aa9d0-125">-NamedValueId</span></span>
<span data-ttu-id="aa9d0-126">명명된 값의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-126">Identifier of the named value.</span></span>
<span data-ttu-id="aa9d0-127">지정된 경우 식별자에 의해 명명된 값을 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="aa9d0-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="aa9d0-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa9d0-129">-Tag</span></span>
<span data-ttu-id="aa9d0-130">태그와 연결된 명명된 값을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="aa9d0-131">지정된 경우 태그와 연결된 모든 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="aa9d0-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="aa9d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9d0-133">CommonParameters</span></span>
<span data-ttu-id="aa9d0-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9d0-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa9d0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9d0-136">입력</span><span class="sxs-lookup"><span data-stu-id="aa9d0-136">INPUTS</span></span>

### <span data-ttu-id="aa9d0-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa9d0-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa9d0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="aa9d0-138">System.String</span></span>

## <span data-ttu-id="aa9d0-139">출력</span><span class="sxs-lookup"><span data-stu-id="aa9d0-139">OUTPUTS</span></span>

### <span data-ttu-id="aa9d0-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="aa9d0-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="aa9d0-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa9d0-141">NOTES</span></span>

## <span data-ttu-id="aa9d0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa9d0-142">RELATED LINKS</span></span>
