---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341486"
---
# <span data-ttu-id="3c6b4-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="3c6b4-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="3c6b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3c6b4-103">그룹에 사용자를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-103">Adds a user to a group.</span></span>

## <span data-ttu-id="3c6b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c6b4-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c6b4-105">설명</span><span class="sxs-lookup"><span data-stu-id="3c6b4-105">DESCRIPTION</span></span>
<span data-ttu-id="3c6b4-106">**Add-AzApiManagementUserToGroup** cmdlet은 그룹에 사용자를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="3c6b4-107">예제</span><span class="sxs-lookup"><span data-stu-id="3c6b4-107">EXAMPLES</span></span>

### <span data-ttu-id="3c6b4-108">예제 1: 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="3c6b4-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="3c6b4-109">이 명령은 기존 사용자를 기존 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="3c6b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c6b4-110">PARAMETERS</span></span>

### <span data-ttu-id="3c6b4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3c6b4-111">-Context</span></span>
<span data-ttu-id="3c6b4-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="3c6b4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="3c6b4-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c6b4-114">-DefaultProfile</span></span>
<span data-ttu-id="3c6b4-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c6b4-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="3c6b4-116">-GroupId</span></span>
<span data-ttu-id="3c6b4-117">그룹 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-117">Specifies the group ID.</span></span>
<span data-ttu-id="3c6b4-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-118">This parameter is required.</span></span>

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

### <span data-ttu-id="3c6b4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c6b4-119">-PassThru</span></span>
<span data-ttu-id="3c6b4-120">passthru</span><span class="sxs-lookup"><span data-stu-id="3c6b4-120">passthru</span></span>

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

### <span data-ttu-id="3c6b4-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="3c6b4-121">-UserId</span></span>
<span data-ttu-id="3c6b4-122">사용자 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-122">Specifies the user ID.</span></span>
<span data-ttu-id="3c6b4-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-123">This parameter is required.</span></span>

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

### <span data-ttu-id="3c6b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c6b4-124">CommonParameters</span></span>
<span data-ttu-id="3c6b4-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c6b4-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c6b4-127">입력</span><span class="sxs-lookup"><span data-stu-id="3c6b4-127">INPUTS</span></span>

### <span data-ttu-id="3c6b4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3c6b4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3c6b4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3c6b4-129">System.String</span></span>

### <span data-ttu-id="3c6b4-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3c6b4-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3c6b4-131">출력</span><span class="sxs-lookup"><span data-stu-id="3c6b4-131">OUTPUTS</span></span>

### <span data-ttu-id="3c6b4-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c6b4-132">System.Boolean</span></span>

## <span data-ttu-id="3c6b4-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c6b4-133">NOTES</span></span>

## <span data-ttu-id="3c6b4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c6b4-134">RELATED LINKS</span></span>

[<span data-ttu-id="3c6b4-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3c6b4-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="3c6b4-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="3c6b4-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


