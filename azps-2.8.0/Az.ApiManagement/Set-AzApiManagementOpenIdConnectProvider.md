---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 880c44e3edf8a5d2c95144d2af8910e73d366192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697931"
---
# <span data-ttu-id="098bf-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="098bf-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="098bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="098bf-102">SYNOPSIS</span></span>
<span data-ttu-id="098bf-103">OpenID Connect provider를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="098bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="098bf-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="098bf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="098bf-105">DESCRIPTION</span></span>
<span data-ttu-id="098bf-106">**Set-AzApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management의 OpenID Connect 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="098bf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="098bf-107">EXAMPLES</span></span>

### <span data-ttu-id="098bf-108">예제 1: 공급자에 대 한 클라이언트 비밀 변경</span><span class="sxs-lookup"><span data-stu-id="098bf-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="098bf-109">이 명령은 ID OICProvider01 인 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-109">This command modifies the provider that has the ID OICProvider01.</span></span>
<span data-ttu-id="098bf-110">명령은 공급자에 대 한 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="098bf-111">변수</span><span class="sxs-lookup"><span data-stu-id="098bf-111">PARAMETERS</span></span>

### <span data-ttu-id="098bf-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="098bf-112">-ClientId</span></span>
<span data-ttu-id="098bf-113">개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="098bf-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="098bf-114">-ClientSecret</span></span>
<span data-ttu-id="098bf-115">개발자 콘솔의 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="098bf-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="098bf-116">-Context</span></span>
<span data-ttu-id="098bf-117">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="098bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098bf-118">-DefaultProfile</span></span>
<span data-ttu-id="098bf-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="098bf-120">-설명</span><span class="sxs-lookup"><span data-stu-id="098bf-120">-Description</span></span>
<span data-ttu-id="098bf-121">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-121">Specifies a description.</span></span>

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

### <span data-ttu-id="098bf-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="098bf-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="098bf-123">공급자의 메타 데이터 끝점 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="098bf-124">-이름</span><span class="sxs-lookup"><span data-stu-id="098bf-124">-Name</span></span>
<span data-ttu-id="098bf-125">공급자에 대 한 친숙 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="098bf-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="098bf-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="098bf-127">이 cmdlet이 수정 하는 공급자에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="098bf-128">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="098bf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="098bf-129">-PassThru</span></span>
<span data-ttu-id="098bf-130">이 cmdlet이이 cmdlet이 수정 하는 **PsApiManagementOpenIdConnectProvider** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="098bf-131">-확인</span><span class="sxs-lookup"><span data-stu-id="098bf-131">-Confirm</span></span>
<span data-ttu-id="098bf-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="098bf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="098bf-133">-WhatIf</span></span>
<span data-ttu-id="098bf-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="098bf-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="098bf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098bf-136">CommonParameters</span></span>
<span data-ttu-id="098bf-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="098bf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098bf-138">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="098bf-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098bf-139">입력</span><span class="sxs-lookup"><span data-stu-id="098bf-139">INPUTS</span></span>

### <span data-ttu-id="098bf-140">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="098bf-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="098bf-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="098bf-141">System.String</span></span>

### <span data-ttu-id="098bf-142">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="098bf-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="098bf-143">출력</span><span class="sxs-lookup"><span data-stu-id="098bf-143">OUTPUTS</span></span>

### <span data-ttu-id="098bf-144">ApiManagement. ServiceManagement. \ PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="098bf-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="098bf-145">상속자</span><span class="sxs-lookup"><span data-stu-id="098bf-145">NOTES</span></span>

## <span data-ttu-id="098bf-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="098bf-146">RELATED LINKS</span></span>

[<span data-ttu-id="098bf-147">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="098bf-147">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="098bf-148">새로운 AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="098bf-148">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="098bf-149">제거-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="098bf-149">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


