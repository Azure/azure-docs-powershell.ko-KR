---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210264"
---
# <span data-ttu-id="26ddf-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="26ddf-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="26ddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="26ddf-103">테넌트 액세스를 활성화 또는 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="26ddf-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="26ddf-104">구문</span><span class="sxs-lookup"><span data-stu-id="26ddf-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26ddf-105">설명</span><span class="sxs-lookup"><span data-stu-id="26ddf-105">DESCRIPTION</span></span>
<span data-ttu-id="26ddf-106">**Set-AzApiManagementTenantAccess** cmdlet은 테넌트 액세스를 활성화하거나 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="26ddf-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="26ddf-107">예제</span><span class="sxs-lookup"><span data-stu-id="26ddf-107">EXAMPLES</span></span>

### <span data-ttu-id="26ddf-108">예제 1: 테넌트 액세스 사용</span><span class="sxs-lookup"><span data-stu-id="26ddf-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="26ddf-109">이 명령을 사용하면 지정된 컨텍스트에서 테넌트에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26ddf-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="26ddf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26ddf-110">PARAMETERS</span></span>

### <span data-ttu-id="26ddf-111">-Context</span><span class="sxs-lookup"><span data-stu-id="26ddf-111">-Context</span></span>
<span data-ttu-id="26ddf-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="26ddf-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="26ddf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ddf-113">-DefaultProfile</span></span>
<span data-ttu-id="26ddf-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26ddf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26ddf-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="26ddf-115">-Enabled</span></span>
<span data-ttu-id="26ddf-116">이 cmdlet이 테넌트 액세스를 활성화 또는 비활성화할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26ddf-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="26ddf-117">사용하지 않도록 설정하거나 $True 값을 $False 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26ddf-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ddf-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26ddf-118">-PassThru</span></span>
<span data-ttu-id="26ddf-119">이 cmdlet이 이 cmdlet이 수정한 **PsApiManagementAccessInformation을** 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26ddf-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="26ddf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ddf-120">CommonParameters</span></span>
<span data-ttu-id="26ddf-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26ddf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ddf-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26ddf-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ddf-123">입력</span><span class="sxs-lookup"><span data-stu-id="26ddf-123">INPUTS</span></span>

### <span data-ttu-id="26ddf-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="26ddf-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26ddf-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="26ddf-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26ddf-126">출력</span><span class="sxs-lookup"><span data-stu-id="26ddf-126">OUTPUTS</span></span>

### <span data-ttu-id="26ddf-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="26ddf-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="26ddf-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26ddf-128">NOTES</span></span>

## <span data-ttu-id="26ddf-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26ddf-129">RELATED LINKS</span></span>

[<span data-ttu-id="26ddf-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="26ddf-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


