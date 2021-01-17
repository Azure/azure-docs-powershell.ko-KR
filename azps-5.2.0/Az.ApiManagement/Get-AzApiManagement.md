---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340130"
---
# <span data-ttu-id="e36ec-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e36ec-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="e36ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e36ec-102">SYNOPSIS</span></span>
<span data-ttu-id="e36ec-103">목록 또는 특정 API Management 서비스 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e36ec-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="e36ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="e36ec-104">SYNTAX</span></span>

### <span data-ttu-id="e36ec-105">GetBySubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="e36ec-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e36ec-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e36ec-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e36ec-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="e36ec-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e36ec-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e36ec-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e36ec-109">설명</span><span class="sxs-lookup"><span data-stu-id="e36ec-109">DESCRIPTION</span></span>
<span data-ttu-id="e36ec-110">**Get-AzApiManagement** cmdlet은 구독 또는 지정된 리소스 그룹 또는 특정 API Management에서 모든 API Management 서비스의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e36ec-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="e36ec-111">예제</span><span class="sxs-lookup"><span data-stu-id="e36ec-111">EXAMPLES</span></span>

### <span data-ttu-id="e36ec-112">예제 1: 모든 API Management 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="e36ec-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="e36ec-113">이 명령은 구독 내의 모든 API Management 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e36ec-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="e36ec-114">예제 2: 특정 이름으로 모든 API Management 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="e36ec-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="e36ec-115">이 명령은 이름에 의해 모든 API Management 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e36ec-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="e36ec-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e36ec-116">PARAMETERS</span></span>

### <span data-ttu-id="e36ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36ec-117">-DefaultProfile</span></span>
<span data-ttu-id="e36ec-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e36ec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e36ec-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e36ec-119">-Name</span></span>
<span data-ttu-id="e36ec-120">API Management 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e36ec-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="e36ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e36ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="e36ec-122">이 cmdlet이 API Management 서비스를 받을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e36ec-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="e36ec-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e36ec-123">-ResourceId</span></span>
<span data-ttu-id="e36ec-124">API Management 서비스의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="e36ec-124">Arm ResourceId of the API Management service.</span></span>

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

### <span data-ttu-id="e36ec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36ec-125">CommonParameters</span></span>
<span data-ttu-id="e36ec-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e36ec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36ec-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e36ec-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36ec-128">입력</span><span class="sxs-lookup"><span data-stu-id="e36ec-128">INPUTS</span></span>

### <span data-ttu-id="e36ec-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e36ec-129">System.String</span></span>

## <span data-ttu-id="e36ec-130">출력</span><span class="sxs-lookup"><span data-stu-id="e36ec-130">OUTPUTS</span></span>

### <span data-ttu-id="e36ec-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e36ec-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e36ec-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e36ec-132">NOTES</span></span>

## <span data-ttu-id="e36ec-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e36ec-133">RELATED LINKS</span></span>

[<span data-ttu-id="e36ec-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e36ec-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="e36ec-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e36ec-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="e36ec-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e36ec-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="e36ec-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e36ec-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


