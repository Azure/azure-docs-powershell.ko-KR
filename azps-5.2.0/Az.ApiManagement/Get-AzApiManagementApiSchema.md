---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338798"
---
# <span data-ttu-id="d7014-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d7014-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="d7014-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7014-102">SYNOPSIS</span></span>
<span data-ttu-id="d7014-103">API Schema의 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="d7014-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="d7014-104">구문</span><span class="sxs-lookup"><span data-stu-id="d7014-104">SYNTAX</span></span>

### <span data-ttu-id="d7014-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d7014-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7014-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7014-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7014-107">설명</span><span class="sxs-lookup"><span data-stu-id="d7014-107">DESCRIPTION</span></span>
<span data-ttu-id="d7014-108">**Get-AzApiManagementApiSchema** cmdlet은 API Schema의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="d7014-109">예제</span><span class="sxs-lookup"><span data-stu-id="d7014-109">EXAMPLES</span></span>

### <span data-ttu-id="d7014-110">예제 1: API의 모든 API Schema에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="d7014-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="d7014-111">이 명령은 특정 ApiManagement 컨텍스트에 대한 API와 연결된 모든 `swagger-petstore-extensive` API 스마마를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="d7014-112">예제 2: API와 연결된 특정 스마마를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-112">Example 2: Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="d7014-113">이 명령은 특정 ApiManagement 컨텍스트에 대한 API와 연결된 `5cc9cf67e6ed3b1154e638bd` `swagger-petstore-extensive` API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="d7014-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7014-114">PARAMETERS</span></span>

### <span data-ttu-id="d7014-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d7014-115">-ApiId</span></span>
<span data-ttu-id="d7014-116">검색할 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-116">API identifier to look for.</span></span>
<span data-ttu-id="d7014-117">지정된 경우 ID로 API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7014-118">-Context</span><span class="sxs-lookup"><span data-stu-id="d7014-118">-Context</span></span>
<span data-ttu-id="d7014-119">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d7014-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7014-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7014-121">-DefaultProfile</span></span>
<span data-ttu-id="d7014-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7014-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7014-123">-ResourceId</span></span>
<span data-ttu-id="d7014-124">Api Schema의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="d7014-125">지정된 경우 식별자에 의해 API 스마마를 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="d7014-126">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-126">This parameter is required.</span></span>

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

### <span data-ttu-id="d7014-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="d7014-127">-SchemaId</span></span>
<span data-ttu-id="d7014-128">Schema의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7014-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7014-129">CommonParameters</span></span>
<span data-ttu-id="d7014-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d7014-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7014-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d7014-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7014-132">입력</span><span class="sxs-lookup"><span data-stu-id="d7014-132">INPUTS</span></span>

### <span data-ttu-id="d7014-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d7014-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7014-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d7014-134">System.String</span></span>

## <span data-ttu-id="d7014-135">출력</span><span class="sxs-lookup"><span data-stu-id="d7014-135">OUTPUTS</span></span>

### <span data-ttu-id="d7014-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d7014-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="d7014-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d7014-137">NOTES</span></span>

## <span data-ttu-id="d7014-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7014-138">RELATED LINKS</span></span>

[<span data-ttu-id="d7014-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d7014-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="d7014-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d7014-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="d7014-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d7014-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)