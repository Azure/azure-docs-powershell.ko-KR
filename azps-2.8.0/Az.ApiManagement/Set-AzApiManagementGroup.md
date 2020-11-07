---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: 2508732b703edf8a4251d305f4bc721eeeed70c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697939"
---
# <span data-ttu-id="be58f-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="be58f-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="be58f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be58f-102">SYNOPSIS</span></span>
<span data-ttu-id="be58f-103">API 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-103">Configures an API management group.</span></span>

## <span data-ttu-id="be58f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be58f-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be58f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be58f-105">DESCRIPTION</span></span>
<span data-ttu-id="be58f-106">**AzApiManagementGroup** CMDLET은 API 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="be58f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be58f-107">EXAMPLES</span></span>

### <span data-ttu-id="be58f-108">예제 1: 관리 그룹 구성</span><span class="sxs-lookup"><span data-stu-id="be58f-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="be58f-109">이 명령은 Group0001 이라는 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="be58f-110">변수</span><span class="sxs-lookup"><span data-stu-id="be58f-110">PARAMETERS</span></span>

### <span data-ttu-id="be58f-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="be58f-111">-Context</span></span>
<span data-ttu-id="be58f-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="be58f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be58f-113">-DefaultProfile</span></span>
<span data-ttu-id="be58f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be58f-115">-설명</span><span class="sxs-lookup"><span data-stu-id="be58f-115">-Description</span></span>
<span data-ttu-id="be58f-116">관리 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="be58f-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="be58f-117">-GroupId</span></span>
<span data-ttu-id="be58f-118">관리 그룹의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="be58f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="be58f-119">-Name</span></span>
<span data-ttu-id="be58f-120">관리 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="be58f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be58f-121">-PassThru</span></span>
<span data-ttu-id="be58f-122">passthru</span><span class="sxs-lookup"><span data-stu-id="be58f-122">passthru</span></span>

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

### <span data-ttu-id="be58f-123">-확인</span><span class="sxs-lookup"><span data-stu-id="be58f-123">-Confirm</span></span>
<span data-ttu-id="be58f-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be58f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be58f-125">-WhatIf</span></span>
<span data-ttu-id="be58f-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be58f-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be58f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be58f-128">CommonParameters</span></span>
<span data-ttu-id="be58f-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be58f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be58f-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be58f-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be58f-131">입력</span><span class="sxs-lookup"><span data-stu-id="be58f-131">INPUTS</span></span>

### <span data-ttu-id="be58f-132">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="be58f-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="be58f-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be58f-133">System.String</span></span>

### <span data-ttu-id="be58f-134">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="be58f-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="be58f-135">출력</span><span class="sxs-lookup"><span data-stu-id="be58f-135">OUTPUTS</span></span>

### <span data-ttu-id="be58f-136">ApiManagement. ServiceManagement. \ PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="be58f-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="be58f-137">상속자</span><span class="sxs-lookup"><span data-stu-id="be58f-137">NOTES</span></span>

## <span data-ttu-id="be58f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be58f-138">RELATED LINKS</span></span>

[<span data-ttu-id="be58f-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="be58f-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="be58f-140">새로운 AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="be58f-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="be58f-141">제거-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="be58f-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


