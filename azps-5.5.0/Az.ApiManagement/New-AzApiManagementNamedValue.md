---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190361"
---
# <span data-ttu-id="aebe2-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="aebe2-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="aebe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aebe2-102">SYNOPSIS</span></span>
<span data-ttu-id="aebe2-103">새 명명된 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-103">Creates new Named Value.</span></span>

## <span data-ttu-id="aebe2-104">구문</span><span class="sxs-lookup"><span data-stu-id="aebe2-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aebe2-105">설명</span><span class="sxs-lookup"><span data-stu-id="aebe2-105">DESCRIPTION</span></span>
<span data-ttu-id="aebe2-106">**New-AzApiManagementNamedValue** cmdlet은 Azure API Management 명명된 **값을 만듭니다.**</span><span class="sxs-lookup"><span data-stu-id="aebe2-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="aebe2-107">예제</span><span class="sxs-lookup"><span data-stu-id="aebe2-107">EXAMPLES</span></span>

### <span data-ttu-id="aebe2-108">예제 1: 태그를 포함하는 명명된 값 만들기</span><span class="sxs-lookup"><span data-stu-id="aebe2-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="aebe2-109">첫 번째 명령은 변수 변수에 두 $Tags 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="aebe2-110">두 번째 명령은 명명된 값을 만들고 속성에 대한 태그로 $Tags 문자열을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="aebe2-111">예제 2: 비밀 값이 있는 명명된 값 만들기</span><span class="sxs-lookup"><span data-stu-id="aebe2-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="aebe2-112">이 명령은 **암호화된** 값이 있는 명명된 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="aebe2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aebe2-113">PARAMETERS</span></span>

### <span data-ttu-id="aebe2-114">-Context</span><span class="sxs-lookup"><span data-stu-id="aebe2-114">-Context</span></span>
<span data-ttu-id="aebe2-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aebe2-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-116">This parameter is required.</span></span>

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

### <span data-ttu-id="aebe2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aebe2-117">-DefaultProfile</span></span>
<span data-ttu-id="aebe2-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aebe2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="aebe2-119">-Name</span></span>
<span data-ttu-id="aebe2-120">명명된 값의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-120">Name of the named value.</span></span>
<span data-ttu-id="aebe2-121">최대 길이는 100자입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="aebe2-122">문자, 숫자, 마주, 대시 및 밑면 문자만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="aebe2-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-123">This parameter is required.</span></span>

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

### <span data-ttu-id="aebe2-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="aebe2-124">-NamedValueId</span></span>
<span data-ttu-id="aebe2-125">새 명명된 값의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-125">Identifier of new named value.</span></span>
<span data-ttu-id="aebe2-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-126">This parameter is optional.</span></span>
<span data-ttu-id="aebe2-127">지정하지 않으면 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="aebe2-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="aebe2-128">-Secret</span></span>
<span data-ttu-id="aebe2-129">값이 비밀인지, 암호화해야 하는지 여부를 판단합니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="aebe2-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-130">This parameter is optional.</span></span>
<span data-ttu-id="aebe2-131">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-131">Default Value is false.</span></span>

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

### <span data-ttu-id="aebe2-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="aebe2-132">-Tag</span></span>
<span data-ttu-id="aebe2-133">명명된 값과 연결될 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="aebe2-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="aebe2-135">-Value</span><span class="sxs-lookup"><span data-stu-id="aebe2-135">-Value</span></span>
<span data-ttu-id="aebe2-136">명명된 값의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-136">Value of the named value.</span></span>
<span data-ttu-id="aebe2-137">정책 식을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-137">Can contain policy expressions.</span></span>
<span data-ttu-id="aebe2-138">최대 길이는 1000자입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="aebe2-139">비어 있거나 공백으로만 구성되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="aebe2-140">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-140">This parameter is required.</span></span>

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

### <span data-ttu-id="aebe2-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aebe2-141">-Confirm</span></span>
<span data-ttu-id="aebe2-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aebe2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aebe2-143">-WhatIf</span></span>
<span data-ttu-id="aebe2-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aebe2-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aebe2-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aebe2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aebe2-146">CommonParameters</span></span>
<span data-ttu-id="aebe2-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aebe2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aebe2-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aebe2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aebe2-149">입력</span><span class="sxs-lookup"><span data-stu-id="aebe2-149">INPUTS</span></span>

### <span data-ttu-id="aebe2-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aebe2-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aebe2-151">System.String</span><span class="sxs-lookup"><span data-stu-id="aebe2-151">System.String</span></span>

### <span data-ttu-id="aebe2-152">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aebe2-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="aebe2-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="aebe2-153">System.String[]</span></span>

## <span data-ttu-id="aebe2-154">출력</span><span class="sxs-lookup"><span data-stu-id="aebe2-154">OUTPUTS</span></span>

### <span data-ttu-id="aebe2-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="aebe2-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="aebe2-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aebe2-156">NOTES</span></span>

## <span data-ttu-id="aebe2-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aebe2-157">RELATED LINKS</span></span>
