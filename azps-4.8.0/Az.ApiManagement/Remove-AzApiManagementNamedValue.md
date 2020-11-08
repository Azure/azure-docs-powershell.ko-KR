---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048541"
---
# <span data-ttu-id="1f9fa-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="1f9fa-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="1f9fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="1f9fa-103">API Management 명명 된 값을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="1f9fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f9fa-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f9fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1f9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="1f9fa-106">**AzApiManagementNamedValue** Cmdlet은 Azure API Management **이라는 값** 을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="1f9fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1f9fa-107">EXAMPLES</span></span>

### <span data-ttu-id="1f9fa-108">예제 1: 명명 된 값 제거</span><span class="sxs-lookup"><span data-stu-id="1f9fa-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="1f9fa-109">이 명령은 ID Property11 인 명명 된 값을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="1f9fa-110">변수</span><span class="sxs-lookup"><span data-stu-id="1f9fa-110">PARAMETERS</span></span>

### <span data-ttu-id="1f9fa-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1f9fa-111">-Context</span></span>
<span data-ttu-id="1f9fa-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1f9fa-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1f9fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f9fa-114">-DefaultProfile</span></span>
<span data-ttu-id="1f9fa-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f9fa-116">-Named= Eid</span><span class="sxs-lookup"><span data-stu-id="1f9fa-116">-NamedValueId</span></span>
<span data-ttu-id="1f9fa-117">기존 명명 된 값의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-117">Identifier of existing named value.</span></span>
<span data-ttu-id="1f9fa-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9fa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f9fa-119">-PassThru</span></span>
<span data-ttu-id="1f9fa-120">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="1f9fa-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-121">This parameter is optional.</span></span>
<span data-ttu-id="1f9fa-122">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-122">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9fa-123">-확인</span><span class="sxs-lookup"><span data-stu-id="1f9fa-123">-Confirm</span></span>
<span data-ttu-id="1f9fa-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9fa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f9fa-125">-WhatIf</span></span>
<span data-ttu-id="1f9fa-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f9fa-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f9fa-128">CommonParameters</span></span>
<span data-ttu-id="1f9fa-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f9fa-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f9fa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f9fa-131">입력</span><span class="sxs-lookup"><span data-stu-id="1f9fa-131">INPUTS</span></span>

### <span data-ttu-id="1f9fa-132">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1f9fa-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1f9fa-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f9fa-133">System.String</span></span>

### <span data-ttu-id="1f9fa-134">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1f9fa-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1f9fa-135">출력</span><span class="sxs-lookup"><span data-stu-id="1f9fa-135">OUTPUTS</span></span>

### <span data-ttu-id="1f9fa-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1f9fa-136">System.Boolean</span></span>

## <span data-ttu-id="1f9fa-137">상속자</span><span class="sxs-lookup"><span data-stu-id="1f9fa-137">NOTES</span></span>

## <span data-ttu-id="1f9fa-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f9fa-138">RELATED LINKS</span></span>
