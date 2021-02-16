---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195460"
---
# <span data-ttu-id="c9f46-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c9f46-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="c9f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9f46-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f46-103">삭제된 웹앱을 새 웹앱 또는 기존 웹앱으로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="c9f46-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9f46-104">SYNTAX</span></span>

### <span data-ttu-id="c9f46-105">FromDeletedResourceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c9f46-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f46-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="c9f46-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9f46-107">설명</span><span class="sxs-lookup"><span data-stu-id="c9f46-107">DESCRIPTION</span></span>
<span data-ttu-id="c9f46-108">**Restore-AzDeletedWebApp** cmdlet은 삭제된 웹앱을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="c9f46-109">TargetResourceGroupName, TargetName 및 TargetSlot에서 지정한 웹앱은 삭제된 웹앱의 내용 및 설정으로 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="c9f46-110">대상 매개 변수를 지정하지 않으면 삭제된 웹앱의 리소스 그룹, 이름 및 슬롯으로 자동으로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="c9f46-111">대상 웹앱이 없는 경우 TargetAppServicePlanName에서 지정한 앱 서비스 계획에 자동으로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="c9f46-112">RestoreContentOnly 스위치 매개 변수를 사용하여 앱 설정 없이 삭제된 앱의 파일만 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="c9f46-113">예제</span><span class="sxs-lookup"><span data-stu-id="c9f46-113">EXAMPLES</span></span>

### <span data-ttu-id="c9f46-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="c9f46-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="c9f46-115">리소스 그룹 Default-Web-WestUS에 속하는 ContosoApp이라는 삭제된 앱을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c9f46-116">이름이 같고 리소스 그룹이 같은 새 앱이 ContosoPlan이라는 App Service 계획에 만들어지며 삭제된 앱의 파일 및 설정이 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="c9f46-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="c9f46-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="c9f46-118">리소스 그룹 Default-Web-WestUS에 속하는 ContosoApp이라는 삭제된 앱의 스테이징 슬롯을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c9f46-119">Default-Web-EastUS 리소스 그룹에 속하는 ContosoRestore라는 웹앱을 덮어 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="c9f46-120">삭제된 웹앱 설정은 복원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="c9f46-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="c9f46-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="c9f46-122">이름이 같은 2개 삭제된 앱이 있는 경우(ContosoApp) 두 사이트에 대한 세부 정보를 얻을 수 있으며 ID를 사용하여 복원을 호출하여 선택한 앱으로 ContosoRestore라는 앱을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="c9f46-123">예제 4</span><span class="sxs-lookup"><span data-stu-id="c9f46-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="c9f46-124">이름이 같은 2개 삭제된 앱이 있는 경우(ContosoApp) 두 사이트에 대한 세부 정보를 얻을 수 있으며, InputObject(Deletedsite) 세부 정보로 복원을 호출하여 선택한 앱으로 ContosoRestore라는 앱을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="c9f46-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9f46-125">PARAMETERS</span></span>

### <span data-ttu-id="c9f46-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9f46-126">-AsJob</span></span>
<span data-ttu-id="c9f46-127">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c9f46-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9f46-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f46-128">-DefaultProfile</span></span>
<span data-ttu-id="c9f46-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9f46-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="c9f46-130">-DeletedId</span></span>
<span data-ttu-id="c9f46-131">삭제된 Azure Web App의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-131">The Id of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f46-132">-Force</span><span class="sxs-lookup"><span data-stu-id="c9f46-132">-Force</span></span>
<span data-ttu-id="c9f46-133">확인 메시지를 표시하지 않고 복원을 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c9f46-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9f46-134">-InputObject</span></span>
<span data-ttu-id="c9f46-135">삭제된 Azure 웹앱입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-135">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="c9f46-136">-Location</span><span class="sxs-lookup"><span data-stu-id="c9f46-136">-Location</span></span>
<span data-ttu-id="c9f46-137">삭제된 Azure Web App의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-137">The location of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f46-138">-Name</span><span class="sxs-lookup"><span data-stu-id="c9f46-138">-Name</span></span>
<span data-ttu-id="c9f46-139">삭제된 Azure Web App의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-139">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="c9f46-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f46-140">-ResourceGroupName</span></span>
<span data-ttu-id="c9f46-141">삭제된 Azure Web App의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-141">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="c9f46-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="c9f46-142">-RestoreContentOnly</span></span>
<span data-ttu-id="c9f46-143">웹앱의 파일을 복원하지만 설정을 복원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="c9f46-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="c9f46-144">-Slot</span></span>
<span data-ttu-id="c9f46-145">삭제된 Azure 웹앱 슬롯입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-145">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="c9f46-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="c9f46-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="c9f46-147">새 Azure 웹앱에 대한 App Service 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="c9f46-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="c9f46-148">-TargetName</span></span>
<span data-ttu-id="c9f46-149">새 Azure 웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="c9f46-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f46-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="c9f46-151">새 Azure Web App을 포함하는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="c9f46-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="c9f46-152">-TargetSlot</span></span>
<span data-ttu-id="c9f46-153">새 Azure Web App 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="c9f46-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="c9f46-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="c9f46-155">오프라인인 배율 단위에서 삭제된 앱을 복구하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="c9f46-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9f46-156">-Confirm</span></span>
<span data-ttu-id="c9f46-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f46-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f46-158">-WhatIf</span></span>
<span data-ttu-id="c9f46-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c9f46-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9f46-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f46-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f46-161">CommonParameters</span></span>
<span data-ttu-id="c9f46-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f46-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f46-163">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9f46-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f46-164">입력</span><span class="sxs-lookup"><span data-stu-id="c9f46-164">INPUTS</span></span>

### <span data-ttu-id="c9f46-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c9f46-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="c9f46-166">출력</span><span class="sxs-lookup"><span data-stu-id="c9f46-166">OUTPUTS</span></span>

### <span data-ttu-id="c9f46-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c9f46-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9f46-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9f46-168">NOTES</span></span>

## <span data-ttu-id="c9f46-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9f46-169">RELATED LINKS</span></span>

[<span data-ttu-id="c9f46-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c9f46-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)