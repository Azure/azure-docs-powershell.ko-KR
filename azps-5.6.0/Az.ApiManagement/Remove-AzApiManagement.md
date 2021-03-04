---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: daa4169ed077003d2ceb773e2e085e72fb6d1ec8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959152"
---
# <span data-ttu-id="e6973-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e6973-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="e6973-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6973-102">SYNOPSIS</span></span>
<span data-ttu-id="e6973-103">API Management 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-103">Removes an API Management service.</span></span>

## <span data-ttu-id="e6973-104">구문</span><span class="sxs-lookup"><span data-stu-id="e6973-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6973-105">설명</span><span class="sxs-lookup"><span data-stu-id="e6973-105">DESCRIPTION</span></span>
<span data-ttu-id="e6973-106">**Remove-AzApiManagement** cmdlet은 Azure API Management 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="e6973-107">예제</span><span class="sxs-lookup"><span data-stu-id="e6973-107">EXAMPLES</span></span>

### <span data-ttu-id="e6973-108">예제 1: API Management 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="e6973-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="e6973-109">이 명령은 ContosoApi라는 API Management 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="e6973-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e6973-110">PARAMETERS</span></span>

### <span data-ttu-id="e6973-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6973-111">-DefaultProfile</span></span>
<span data-ttu-id="e6973-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6973-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e6973-113">-Name</span></span>
<span data-ttu-id="e6973-114">이 cmdlet이 제거하는 API Management 배포의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e6973-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6973-115">-PassThru</span></span>
<span data-ttu-id="e6973-116">이 cmdlet은 작업이 성공하면 $True 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6973-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6973-117">-ResourceGroupName</span></span>
<span data-ttu-id="e6973-118">API Management 배포가 있는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="e6973-119">-확인</span><span class="sxs-lookup"><span data-stu-id="e6973-119">-Confirm</span></span>
<span data-ttu-id="e6973-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6973-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6973-121">-WhatIf</span></span>
<span data-ttu-id="e6973-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6973-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6973-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6973-124">CommonParameters</span></span>
<span data-ttu-id="e6973-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6973-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6973-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6973-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6973-127">입력</span><span class="sxs-lookup"><span data-stu-id="e6973-127">INPUTS</span></span>

### <span data-ttu-id="e6973-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e6973-128">System.String</span></span>

## <span data-ttu-id="e6973-129">출력</span><span class="sxs-lookup"><span data-stu-id="e6973-129">OUTPUTS</span></span>

### <span data-ttu-id="e6973-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6973-130">System.Boolean</span></span>

## <span data-ttu-id="e6973-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6973-131">NOTES</span></span>

## <span data-ttu-id="e6973-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6973-132">RELATED LINKS</span></span>

[<span data-ttu-id="e6973-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e6973-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="e6973-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e6973-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="e6973-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e6973-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="e6973-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e6973-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


