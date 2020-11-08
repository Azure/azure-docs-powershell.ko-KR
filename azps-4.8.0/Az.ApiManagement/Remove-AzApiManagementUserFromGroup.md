---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204122"
---
# <span data-ttu-id="e5cae-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="e5cae-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="e5cae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5cae-102">SYNOPSIS</span></span>
<span data-ttu-id="e5cae-103">그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5cae-103">Removes a user from a group.</span></span>

## <span data-ttu-id="e5cae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5cae-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5cae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e5cae-105">DESCRIPTION</span></span>
<span data-ttu-id="e5cae-106">**Remove-AzApiManagementUserFromGroup** cmdlet은 기존 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5cae-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="e5cae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e5cae-107">EXAMPLES</span></span>

### <span data-ttu-id="e5cae-108">예제 1: 그룹에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="e5cae-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="e5cae-109">이 명령은 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5cae-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="e5cae-110">변수</span><span class="sxs-lookup"><span data-stu-id="e5cae-110">PARAMETERS</span></span>

### <span data-ttu-id="e5cae-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e5cae-111">-Context</span></span>
<span data-ttu-id="e5cae-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5cae-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="e5cae-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="e5cae-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e5cae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5cae-114">-DefaultProfile</span></span>
<span data-ttu-id="e5cae-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5cae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5cae-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="e5cae-116">-GroupId</span></span>
<span data-ttu-id="e5cae-117">사용자를 제거할 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5cae-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="e5cae-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5cae-118">-PassThru</span></span>
<span data-ttu-id="e5cae-119">이 cmdlet이 $True 값을 반환 하거나, 성공할 경우, $False의 값이 반환 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e5cae-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="e5cae-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="e5cae-120">-UserId</span></span>
<span data-ttu-id="e5cae-121">그룹에서 제거할 사용자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5cae-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="e5cae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5cae-122">CommonParameters</span></span>
<span data-ttu-id="e5cae-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5cae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5cae-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5cae-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5cae-125">입력</span><span class="sxs-lookup"><span data-stu-id="e5cae-125">INPUTS</span></span>

### <span data-ttu-id="e5cae-126">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e5cae-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e5cae-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e5cae-127">System.String</span></span>

### <span data-ttu-id="e5cae-128">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e5cae-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e5cae-129">출력</span><span class="sxs-lookup"><span data-stu-id="e5cae-129">OUTPUTS</span></span>

### <span data-ttu-id="e5cae-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e5cae-130">System.Boolean</span></span>

## <span data-ttu-id="e5cae-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e5cae-131">NOTES</span></span>

## <span data-ttu-id="e5cae-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5cae-132">RELATED LINKS</span></span>

[<span data-ttu-id="e5cae-133">추가-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="e5cae-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="e5cae-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e5cae-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


