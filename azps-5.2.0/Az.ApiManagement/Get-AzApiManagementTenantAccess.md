---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330986"
---
# <span data-ttu-id="1897a-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="1897a-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="1897a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1897a-102">SYNOPSIS</span></span>
<span data-ttu-id="1897a-103">테넌트에 대한 액세스 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1897a-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="1897a-104">구문</span><span class="sxs-lookup"><span data-stu-id="1897a-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1897a-105">설명</span><span class="sxs-lookup"><span data-stu-id="1897a-105">DESCRIPTION</span></span>
<span data-ttu-id="1897a-106">**Get-AzApiManagementTenantAccess** cmdlet은 테넌트에 대한 테넌트 액세스 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1897a-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="1897a-107">키는 결과 세부 정보에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1897a-107">Keys will not be included into result details.</span></span> <span data-ttu-id="1897a-108">클라이언트 비밀을 얻습니다. **Get-AzApiManagementTenantAccessSecret을 사용 합니다.**</span><span class="sxs-lookup"><span data-stu-id="1897a-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="1897a-109">예제</span><span class="sxs-lookup"><span data-stu-id="1897a-109">EXAMPLES</span></span>

### <span data-ttu-id="1897a-110">예제 1: 테넌트 액세스 구성을 얻게</span><span class="sxs-lookup"><span data-stu-id="1897a-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="1897a-111">이 명령은 지정된 컨텍스트에 대한 테넌트 액세스 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1897a-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="1897a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1897a-112">PARAMETERS</span></span>

### <span data-ttu-id="1897a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="1897a-113">-Context</span></span>
<span data-ttu-id="1897a-114">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="1897a-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1897a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1897a-115">-DefaultProfile</span></span>
<span data-ttu-id="1897a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1897a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1897a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1897a-117">CommonParameters</span></span>
<span data-ttu-id="1897a-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1897a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1897a-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1897a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1897a-120">입력</span><span class="sxs-lookup"><span data-stu-id="1897a-120">INPUTS</span></span>

### <span data-ttu-id="1897a-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1897a-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="1897a-122">출력</span><span class="sxs-lookup"><span data-stu-id="1897a-122">OUTPUTS</span></span>

### <span data-ttu-id="1897a-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="1897a-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="1897a-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1897a-124">NOTES</span></span>

## <span data-ttu-id="1897a-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1897a-125">RELATED LINKS</span></span>

[<span data-ttu-id="1897a-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="1897a-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


