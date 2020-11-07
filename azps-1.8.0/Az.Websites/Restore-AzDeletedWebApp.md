---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a90a56417ab8b1b08d72cb9d00ebe7411a6f075c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698304"
---
# <span data-ttu-id="6f6f3-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6f6f3-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="6f6f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6f3-103">삭제 된 웹 앱을 새 또는 기존 웹 앱으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="6f6f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f6f3-104">SYNTAX</span></span>

### <span data-ttu-id="6f6f3-105">FromDeletedResourceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6f6f3-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f6f3-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="6f6f3-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f6f3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6f6f3-107">DESCRIPTION</span></span>
<span data-ttu-id="6f6f3-108">**Restore-AzDeletedWebApp** cmdlet은 삭제 된 웹 앱을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="6f6f3-109">TargetResourceGroupName, TargetName 및 TargetSlot으로 지정 된 웹 앱은 삭제 된 웹 앱의 콘텐츠 및 설정으로 덮어쓰여집니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="6f6f3-110">대상 매개 변수를 지정 하지 않으면 삭제 된 웹 앱의 리소스 그룹, 이름, 슬롯으로 자동으로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="6f6f3-111">대상 웹 앱이 없는 경우 Targetappserviceplan 이름으로 지정 된 앱 서비스 계획에 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="6f6f3-112">RestoreContentOnly switch 매개 변수를 사용 하 여 앱 설정 없이 삭제 된 앱의 파일만 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="6f6f3-113">예제의</span><span class="sxs-lookup"><span data-stu-id="6f6f3-113">EXAMPLES</span></span>

### <span data-ttu-id="6f6f3-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f6f3-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="6f6f3-115">리소스 그룹 기본값-웹-WestUS에 속한 ContosoApp 이라는 삭제 된 앱을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="6f6f3-116">이름 및 리소스 그룹이 같은 새 앱이 ContosoPlan 이라는 앱 서비스 계획에서 만들어지고, 삭제 된 앱의 파일 및 설정이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="6f6f3-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="6f6f3-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="6f6f3-118">리소스 그룹 Default-웹용 WestUS에 속한 ContosoApp 이라는 삭제 된 앱의 준비 슬롯을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="6f6f3-119">리소스 그룹 Default-ContosoRestore에 속한 웹 앱 이라는 이름이 사용자에 게 덮어쓰여집니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="6f6f3-120">삭제 된 웹 앱 설정은 복원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="6f6f3-121">변수</span><span class="sxs-lookup"><span data-stu-id="6f6f3-121">PARAMETERS</span></span>

### <span data-ttu-id="6f6f3-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f6f3-122">-AsJob</span></span>
<span data-ttu-id="6f6f3-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6f6f3-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f6f3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f6f3-124">-DefaultProfile</span></span>
<span data-ttu-id="6f6f3-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f6f3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6f6f3-126">-Force</span></span>
<span data-ttu-id="6f6f3-127">확인 메시지를 표시 하지 않고 복원을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6f6f3-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f6f3-128">-InputObject</span></span>
<span data-ttu-id="6f6f3-129">삭제 된 Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-129">The deleted Azure Web App.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f3-130">-이름</span><span class="sxs-lookup"><span data-stu-id="6f6f3-130">-Name</span></span>
<span data-ttu-id="6f6f3-131">삭제 된 Azure 웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-131">The name of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f6f3-132">-ResourceGroupName</span></span>
<span data-ttu-id="6f6f3-133">삭제 된 Azure Web App의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-133">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f3-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="6f6f3-134">-RestoreContentOnly</span></span>
<span data-ttu-id="6f6f3-135">웹 앱의 파일을 복원 하지만 설정을 복원 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="6f6f3-136">-슬롯</span><span class="sxs-lookup"><span data-stu-id="6f6f3-136">-Slot</span></span>
<span data-ttu-id="6f6f3-137">삭제 된 Azure 웹 앱 슬롯</span><span class="sxs-lookup"><span data-stu-id="6f6f3-137">The deleted Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f3-138">-Targetappservice계획 이름</span><span class="sxs-lookup"><span data-stu-id="6f6f3-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="6f6f3-139">새 Azure 웹 앱에 대 한 앱 서비스 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-139">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f3-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="6f6f3-140">-TargetName</span></span>
<span data-ttu-id="6f6f3-141">새 Azure 웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-141">The name of the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f3-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f6f3-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="6f6f3-143">새 Azure Web App이 포함 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-143">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f3-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="6f6f3-144">-TargetSlot</span></span>
<span data-ttu-id="6f6f3-145">새 Azure Web App 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-145">The name of the new Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6f3-146">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="6f6f3-146">-UseDisasterRecovery</span></span>
<span data-ttu-id="6f6f3-147">오프 라인 상태인 배율 단위에서 삭제 된 앱을 복구 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-147">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="6f6f3-148">-확인</span><span class="sxs-lookup"><span data-stu-id="6f6f3-148">-Confirm</span></span>
<span data-ttu-id="6f6f3-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f6f3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f6f3-150">-WhatIf</span></span>
<span data-ttu-id="6f6f3-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f6f3-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f6f3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6f3-153">CommonParameters</span></span>
<span data-ttu-id="6f6f3-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6f3-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f6f3-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6f3-156">입력</span><span class="sxs-lookup"><span data-stu-id="6f6f3-156">INPUTS</span></span>

### <span data-ttu-id="6f6f3-157">PSAzureDeletedWebApp (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-157">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="6f6f3-158">출력</span><span class="sxs-lookup"><span data-stu-id="6f6f3-158">OUTPUTS</span></span>

### <span data-ttu-id="6f6f3-159">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="6f6f3-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6f6f3-160">상속자</span><span class="sxs-lookup"><span data-stu-id="6f6f3-160">NOTES</span></span>

## <span data-ttu-id="6f6f3-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f6f3-161">RELATED LINKS</span></span>

[<span data-ttu-id="6f6f3-162">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6f6f3-162">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)