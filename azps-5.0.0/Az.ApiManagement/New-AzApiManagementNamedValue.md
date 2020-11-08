---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216929"
---
# <span data-ttu-id="ecb54-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="ecb54-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="ecb54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb54-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb54-103">새 명명 된 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-103">Creates new Named Value.</span></span>

## <span data-ttu-id="ecb54-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecb54-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecb54-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ecb54-105">DESCRIPTION</span></span>
<span data-ttu-id="ecb54-106">**AzApiManagementNamedValue** Cmdlet은 Azure API Management **이라는 값** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="ecb54-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ecb54-107">EXAMPLES</span></span>

### <span data-ttu-id="ecb54-108">예제 1: 태그를 포함 하는 명명 된 값 만들기</span><span class="sxs-lookup"><span data-stu-id="ecb54-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="ecb54-109">첫 번째 명령은 $Tags 변수에 두 개의 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="ecb54-110">두 번째 명령은 명명 된 값을 만들고 해당 문자열을 속성의 태그로 $Tags에 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="ecb54-111">예제 2: 비밀 값이 있는 명명 된 값 만들기</span><span class="sxs-lookup"><span data-stu-id="ecb54-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="ecb54-112">이 명령은 암호화 된 값이 있는 **명명 된 값** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="ecb54-113">변수</span><span class="sxs-lookup"><span data-stu-id="ecb54-113">PARAMETERS</span></span>

### <span data-ttu-id="ecb54-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ecb54-114">-Context</span></span>
<span data-ttu-id="ecb54-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ecb54-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-116">This parameter is required.</span></span>

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

### <span data-ttu-id="ecb54-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb54-117">-DefaultProfile</span></span>
<span data-ttu-id="ecb54-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecb54-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ecb54-119">-Name</span></span>
<span data-ttu-id="ecb54-120">명명 된 값의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-120">Name of the named value.</span></span>
<span data-ttu-id="ecb54-121">최대 길이는 100 자입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="ecb54-122">문자, 숫자, 마침표, 대시, 밑줄 문자만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="ecb54-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-123">This parameter is required.</span></span>

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

### <span data-ttu-id="ecb54-124">-Named= Eid</span><span class="sxs-lookup"><span data-stu-id="ecb54-124">-NamedValueId</span></span>
<span data-ttu-id="ecb54-125">명명 된 새 값의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-125">Identifier of new named value.</span></span>
<span data-ttu-id="ecb54-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-126">This parameter is optional.</span></span>
<span data-ttu-id="ecb54-127">지정 하지 않으면가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="ecb54-128">-비밀</span><span class="sxs-lookup"><span data-stu-id="ecb54-128">-Secret</span></span>
<span data-ttu-id="ecb54-129">값이 비밀이 고 암호화 해야 하는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="ecb54-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-130">This parameter is optional.</span></span>
<span data-ttu-id="ecb54-131">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-131">Default Value is false.</span></span>

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

### <span data-ttu-id="ecb54-132">태그</span><span class="sxs-lookup"><span data-stu-id="ecb54-132">-Tag</span></span>
<span data-ttu-id="ecb54-133">명명 된 값과 연결 되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="ecb54-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb54-135">-값</span><span class="sxs-lookup"><span data-stu-id="ecb54-135">-Value</span></span>
<span data-ttu-id="ecb54-136">명명 된 값의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-136">Value of the named value.</span></span>
<span data-ttu-id="ecb54-137">정책 식을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-137">Can contain policy expressions.</span></span>
<span data-ttu-id="ecb54-138">최대 길이는 1000 자입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="ecb54-139">비어 있지 않거나 공백으로만 구성 되지 않았을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="ecb54-140">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-140">This parameter is required.</span></span>

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

### <span data-ttu-id="ecb54-141">-확인</span><span class="sxs-lookup"><span data-stu-id="ecb54-141">-Confirm</span></span>
<span data-ttu-id="ecb54-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb54-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb54-143">-WhatIf</span></span>
<span data-ttu-id="ecb54-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecb54-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb54-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb54-146">CommonParameters</span></span>
<span data-ttu-id="ecb54-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb54-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb54-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ecb54-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb54-149">입력</span><span class="sxs-lookup"><span data-stu-id="ecb54-149">INPUTS</span></span>

### <span data-ttu-id="ecb54-150">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ecb54-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ecb54-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ecb54-151">System.String</span></span>

### <span data-ttu-id="ecb54-152">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ecb54-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ecb54-153">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="ecb54-153">System.String[]</span></span>

## <span data-ttu-id="ecb54-154">출력</span><span class="sxs-lookup"><span data-stu-id="ecb54-154">OUTPUTS</span></span>

### <span data-ttu-id="ecb54-155">ApiManagement. ServiceManagement. \ PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="ecb54-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="ecb54-156">상속자</span><span class="sxs-lookup"><span data-stu-id="ecb54-156">NOTES</span></span>

## <span data-ttu-id="ecb54-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecb54-157">RELATED LINKS</span></span>
