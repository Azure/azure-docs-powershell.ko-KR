---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: e27dcc838499e742c887f60a30021d8ac99277f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216554"
---
# <span data-ttu-id="9a7f0-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9a7f0-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="9a7f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7f0-103">Azure active directory 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="9a7f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a7f0-104">SYNTAX</span></span>

### <span data-ttu-id="9a7f0-105">ObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a7f0-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7f0-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a7f0-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7f0-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a7f0-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7f0-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a7f0-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a7f0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9a7f0-109">DESCRIPTION</span></span>
<span data-ttu-id="9a7f0-110">Azure active directory 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="9a7f0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9a7f0-111">EXAMPLES</span></span>

### <span data-ttu-id="9a7f0-112">예제 1: 개체 id를 기준으로 응용 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="9a7f0-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="9a7f0-113">테 넌 트에서 개체 id가 ' b4cd1619-80b3-4cfb-9f8f-9f2333425738 ' 인 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="9a7f0-114">예제 2: 응용 프로그램 id를 기준으로 응용 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="9a7f0-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="9a7f0-115">테 넌 트에서 응용 프로그램 id가 ' f9c5ea4f-28f0-401a-a491-491a037fa346 ' 인 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="9a7f0-116">예제 3: 파이핑을 기준으로 응용 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="9a7f0-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="9a7f0-117">개체 id가 ' b4cd1619-80b3-4cfb-9f8f-9f2333425738 ' 인 응용 프로그램을 가져오고, 테 넌 트에서 응용 프로그램을 제거 하도록 Remove-AzADApplication cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="9a7f0-118">변수</span><span class="sxs-lookup"><span data-stu-id="9a7f0-118">PARAMETERS</span></span>

### <span data-ttu-id="9a7f0-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9a7f0-119">-ApplicationId</span></span>
<span data-ttu-id="9a7f0-120">제거할 응용 프로그램의 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-120">The application id of the application to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a7f0-121">-DefaultProfile</span></span>
<span data-ttu-id="9a7f0-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9a7f0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a7f0-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9a7f0-123">-DisplayName</span></span>
<span data-ttu-id="9a7f0-124">응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7f0-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9a7f0-125">-Force</span></span>
<span data-ttu-id="9a7f0-126">확인 없이 응용 프로그램 삭제로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="9a7f0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a7f0-127">-InputObject</span></span>
<span data-ttu-id="9a7f0-128">제거할 응용 프로그램을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7f0-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9a7f0-129">-ObjectId</span></span>
<span data-ttu-id="9a7f0-130">삭제할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-130">The object id of the application to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7f0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a7f0-131">-PassThru</span></span>
<span data-ttu-id="9a7f0-132">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9a7f0-133">-확인</span><span class="sxs-lookup"><span data-stu-id="9a7f0-133">-Confirm</span></span>
<span data-ttu-id="9a7f0-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a7f0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a7f0-135">-WhatIf</span></span>
<span data-ttu-id="9a7f0-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a7f0-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a7f0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7f0-138">CommonParameters</span></span>
<span data-ttu-id="9a7f0-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7f0-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a7f0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7f0-141">입력</span><span class="sxs-lookup"><span data-stu-id="9a7f0-141">INPUTS</span></span>

### <span data-ttu-id="9a7f0-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a7f0-142">System.String</span></span>

### <span data-ttu-id="9a7f0-143">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="9a7f0-143">System.Guid</span></span>

### <span data-ttu-id="9a7f0-144">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="9a7f0-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="9a7f0-145">출력</span><span class="sxs-lookup"><span data-stu-id="9a7f0-145">OUTPUTS</span></span>

### <span data-ttu-id="9a7f0-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9a7f0-146">System.Boolean</span></span>

## <span data-ttu-id="9a7f0-147">상속자</span><span class="sxs-lookup"><span data-stu-id="9a7f0-147">NOTES</span></span>
<span data-ttu-id="9a7f0-148">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="9a7f0-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9a7f0-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a7f0-149">RELATED LINKS</span></span>

[<span data-ttu-id="9a7f0-150">새로운 AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9a7f0-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="9a7f0-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9a7f0-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="9a7f0-152">업데이트-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9a7f0-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="9a7f0-153">제거-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9a7f0-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

