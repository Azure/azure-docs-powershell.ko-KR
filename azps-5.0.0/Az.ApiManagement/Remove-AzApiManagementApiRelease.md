---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309346"
---
# <span data-ttu-id="57350-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="57350-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="57350-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57350-102">SYNOPSIS</span></span>
<span data-ttu-id="57350-103">특정 API 릴리스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57350-103">Removes a particular API Release</span></span>

## <span data-ttu-id="57350-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57350-104">SYNTAX</span></span>

### <span data-ttu-id="57350-105">ByApiReleaseId (기본값)</span><span class="sxs-lookup"><span data-stu-id="57350-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57350-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="57350-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57350-107">설명은</span><span class="sxs-lookup"><span data-stu-id="57350-107">DESCRIPTION</span></span>

<span data-ttu-id="57350-108">**AzAzureRmApiManagementApiRelease** cmdlet은 기존 API 릴리스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57350-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="57350-109">예제의</span><span class="sxs-lookup"><span data-stu-id="57350-109">EXAMPLES</span></span>

### <span data-ttu-id="57350-110">예제 1: API 릴리스 제거</span><span class="sxs-lookup"><span data-stu-id="57350-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="57350-111">이 명령은 지정 된 ApiId 및 ReleaseId를 사용 하 여 API Release를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57350-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="57350-112">변수</span><span class="sxs-lookup"><span data-stu-id="57350-112">PARAMETERS</span></span>

### <span data-ttu-id="57350-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="57350-113">-ApiId</span></span>
<span data-ttu-id="57350-114">API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="57350-114">Identifier of the API.</span></span>
<span data-ttu-id="57350-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="57350-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57350-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="57350-116">-Context</span></span>
<span data-ttu-id="57350-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="57350-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="57350-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="57350-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57350-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57350-119">-DefaultProfile</span></span>
<span data-ttu-id="57350-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57350-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57350-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57350-121">-InputObject</span></span>
<span data-ttu-id="57350-122">PsApiManagementApiRelease의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="57350-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="57350-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="57350-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57350-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57350-124">-PassThru</span></span>
<span data-ttu-id="57350-125">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="57350-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="57350-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="57350-126">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57350-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="57350-127">-ReleaseId</span></span>
<span data-ttu-id="57350-128">API 릴리스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="57350-128">Identifier of the API Release.</span></span>
<span data-ttu-id="57350-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="57350-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57350-130">-확인</span><span class="sxs-lookup"><span data-stu-id="57350-130">-Confirm</span></span>
<span data-ttu-id="57350-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57350-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57350-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57350-132">-WhatIf</span></span>
<span data-ttu-id="57350-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57350-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57350-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57350-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57350-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57350-135">CommonParameters</span></span>
<span data-ttu-id="57350-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57350-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57350-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57350-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57350-138">입력</span><span class="sxs-lookup"><span data-stu-id="57350-138">INPUTS</span></span>

### <span data-ttu-id="57350-139">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="57350-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="57350-140">ApiManagement. ServiceManagement. \ PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="57350-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="57350-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="57350-141">System.String</span></span>

## <span data-ttu-id="57350-142">출력</span><span class="sxs-lookup"><span data-stu-id="57350-142">OUTPUTS</span></span>

### <span data-ttu-id="57350-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="57350-143">System.Boolean</span></span>

## <span data-ttu-id="57350-144">상속자</span><span class="sxs-lookup"><span data-stu-id="57350-144">NOTES</span></span>

## <span data-ttu-id="57350-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57350-145">RELATED LINKS</span></span>

[<span data-ttu-id="57350-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="57350-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="57350-147">새로운 AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="57350-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="57350-148">업데이트-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="57350-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)