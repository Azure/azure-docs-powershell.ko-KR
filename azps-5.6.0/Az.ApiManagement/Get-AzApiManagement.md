---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: a4a6cf459c253c26f5d550492f8b756d59fcdf44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994616"
---
# <span data-ttu-id="f8dfc-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8dfc-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="f8dfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="f8dfc-103">목록 또는 특정 API Management Service 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f8dfc-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="f8dfc-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8dfc-104">SYNTAX</span></span>

### <span data-ttu-id="f8dfc-105">GetBySubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="f8dfc-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8dfc-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8dfc-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8dfc-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="f8dfc-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8dfc-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f8dfc-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8dfc-109">설명</span><span class="sxs-lookup"><span data-stu-id="f8dfc-109">DESCRIPTION</span></span>
<span data-ttu-id="f8dfc-110">**Get-AzApiManagement** cmdlet은 구독 또는 지정된 리소스 그룹 또는 특정 API Management에서 모든 API Management 서비스의 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f8dfc-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="f8dfc-111">예제</span><span class="sxs-lookup"><span data-stu-id="f8dfc-111">EXAMPLES</span></span>

### <span data-ttu-id="f8dfc-112">예제 1: 모든 API Management 서비스 사용</span><span class="sxs-lookup"><span data-stu-id="f8dfc-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="f8dfc-113">이 명령은 구독 내의 모든 API Management 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f8dfc-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="f8dfc-114">예제 2: 특정 이름으로 모든 API Management 서비스 사용</span><span class="sxs-lookup"><span data-stu-id="f8dfc-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="f8dfc-115">이 명령은 모든 API Management 서비스를 이름으로 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f8dfc-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="f8dfc-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f8dfc-116">PARAMETERS</span></span>

### <span data-ttu-id="f8dfc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8dfc-117">-DefaultProfile</span></span>
<span data-ttu-id="f8dfc-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8dfc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8dfc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f8dfc-119">-Name</span></span>
<span data-ttu-id="f8dfc-120">API Management 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8dfc-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="f8dfc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8dfc-121">-ResourceGroupName</span></span>
<span data-ttu-id="f8dfc-122">이 cmdlet에서 API Management 서비스를 제공하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8dfc-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="f8dfc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8dfc-123">-ResourceId</span></span>
<span data-ttu-id="f8dfc-124">API Management 서비스의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="f8dfc-124">Arm ResourceId of the API Management service.</span></span>

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

### <span data-ttu-id="f8dfc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8dfc-125">CommonParameters</span></span>
<span data-ttu-id="f8dfc-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8dfc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8dfc-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8dfc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8dfc-128">입력</span><span class="sxs-lookup"><span data-stu-id="f8dfc-128">INPUTS</span></span>

### <span data-ttu-id="f8dfc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f8dfc-129">System.String</span></span>

## <span data-ttu-id="f8dfc-130">출력</span><span class="sxs-lookup"><span data-stu-id="f8dfc-130">OUTPUTS</span></span>

### <span data-ttu-id="f8dfc-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8dfc-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f8dfc-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8dfc-132">NOTES</span></span>

## <span data-ttu-id="f8dfc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8dfc-133">RELATED LINKS</span></span>

[<span data-ttu-id="f8dfc-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8dfc-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="f8dfc-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8dfc-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="f8dfc-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8dfc-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="f8dfc-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f8dfc-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


