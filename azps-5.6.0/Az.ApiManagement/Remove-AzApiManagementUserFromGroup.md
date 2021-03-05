---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 03073dc6116595c93b2c25d30b38c5467482903c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010955"
---
# <span data-ttu-id="98d40-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="98d40-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="98d40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98d40-102">SYNOPSIS</span></span>
<span data-ttu-id="98d40-103">그룹에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="98d40-103">Removes a user from a group.</span></span>

## <span data-ttu-id="98d40-104">구문</span><span class="sxs-lookup"><span data-stu-id="98d40-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98d40-105">설명</span><span class="sxs-lookup"><span data-stu-id="98d40-105">DESCRIPTION</span></span>
<span data-ttu-id="98d40-106">**Remove-AzApiManagementUserFromGroup** cmdlet은 기존 그룹에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="98d40-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="98d40-107">예제</span><span class="sxs-lookup"><span data-stu-id="98d40-107">EXAMPLES</span></span>

### <span data-ttu-id="98d40-108">예제 1: 그룹에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="98d40-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="98d40-109">이 명령은 그룹에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="98d40-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="98d40-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="98d40-110">PARAMETERS</span></span>

### <span data-ttu-id="98d40-111">-Context</span><span class="sxs-lookup"><span data-stu-id="98d40-111">-Context</span></span>
<span data-ttu-id="98d40-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="98d40-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="98d40-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="98d40-113">This parameter is required.</span></span>

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

### <span data-ttu-id="98d40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d40-114">-DefaultProfile</span></span>
<span data-ttu-id="98d40-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98d40-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98d40-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="98d40-116">-GroupId</span></span>
<span data-ttu-id="98d40-117">사용자를 제거할 그룹의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98d40-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="98d40-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98d40-118">-PassThru</span></span>
<span data-ttu-id="98d40-119">이 cmdlet은 성공하는 경우 $True 값을 반환하거나, 그렇지 않은 경우 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="98d40-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="98d40-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="98d40-120">-UserId</span></span>
<span data-ttu-id="98d40-121">그룹에서 제거할 사용자의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98d40-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="98d40-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d40-122">CommonParameters</span></span>
<span data-ttu-id="98d40-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98d40-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d40-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98d40-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d40-125">입력</span><span class="sxs-lookup"><span data-stu-id="98d40-125">INPUTS</span></span>

### <span data-ttu-id="98d40-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98d40-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98d40-127">System.String</span><span class="sxs-lookup"><span data-stu-id="98d40-127">System.String</span></span>

### <span data-ttu-id="98d40-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98d40-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="98d40-129">출력</span><span class="sxs-lookup"><span data-stu-id="98d40-129">OUTPUTS</span></span>

### <span data-ttu-id="98d40-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98d40-130">System.Boolean</span></span>

## <span data-ttu-id="98d40-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98d40-131">NOTES</span></span>

## <span data-ttu-id="98d40-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98d40-132">RELATED LINKS</span></span>

[<span data-ttu-id="98d40-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="98d40-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="98d40-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="98d40-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


