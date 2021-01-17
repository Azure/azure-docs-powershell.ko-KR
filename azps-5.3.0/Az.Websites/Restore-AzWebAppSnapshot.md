---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491420"
---
# <span data-ttu-id="1e11e-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1e11e-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="1e11e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e11e-102">SYNOPSIS</span></span>
<span data-ttu-id="1e11e-103">웹앱 스냅숏을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="1e11e-104">구문</span><span class="sxs-lookup"><span data-stu-id="1e11e-104">SYNTAX</span></span>

### <span data-ttu-id="1e11e-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1e11e-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e11e-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1e11e-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e11e-107">설명</span><span class="sxs-lookup"><span data-stu-id="1e11e-107">DESCRIPTION</span></span>
<span data-ttu-id="1e11e-108">웹앱 스냅숏을 웹앱으로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="1e11e-109">스냅숏을 복원하면 웹앱의 모든 파일을 스냅숏에 포함된 파일로 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="1e11e-110">설정도 복원하려면 RecoverConfiguration 스위치 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="1e11e-111">한 웹앱의 스냅숏을 동일한 구독의 다른 웹앱으로 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="1e11e-112">예제</span><span class="sxs-lookup"><span data-stu-id="1e11e-112">EXAMPLES</span></span>

### <span data-ttu-id="1e11e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="1e11e-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="1e11e-114">"Default-Web-WestUS" 리소스 그룹에 "스테이징"이라는 슬롯이 있는 "ContosoApp"이라는 웹앱의 최신 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="1e11e-115">스냅숏을 웹앱의 "복원" 슬롯으로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="1e11e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e11e-116">PARAMETERS</span></span>

### <span data-ttu-id="1e11e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e11e-117">-AsJob</span></span>
<span data-ttu-id="1e11e-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1e11e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e11e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e11e-119">-DefaultProfile</span></span>
<span data-ttu-id="1e11e-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e11e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1e11e-121">-Force</span></span>
<span data-ttu-id="1e11e-122">경고를 표시하지 않고 원래 웹앱을 덮어 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="1e11e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e11e-123">-InputObject</span></span>
<span data-ttu-id="1e11e-124">Azure 웹앱 스냅숏입니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-124">The Azure Web App snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e11e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1e11e-125">-Name</span></span>
<span data-ttu-id="1e11e-126">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-126">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e11e-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e11e-127">-RecoverConfiguration</span></span>
<span data-ttu-id="1e11e-128">파일 외에도 웹앱의 구성을 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="1e11e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e11e-129">-ResourceGroupName</span></span>
<span data-ttu-id="1e11e-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e11e-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="1e11e-131">-Slot</span></span>
<span data-ttu-id="1e11e-132">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-132">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e11e-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="1e11e-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="1e11e-134">오프라인인 배율 단위에서 스냅숏을 복구하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="1e11e-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1e11e-135">-WebApp</span></span>
<span data-ttu-id="1e11e-136">웹앱 개체</span><span class="sxs-lookup"><span data-stu-id="1e11e-136">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e11e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e11e-137">-Confirm</span></span>
<span data-ttu-id="1e11e-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e11e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e11e-139">-WhatIf</span></span>
<span data-ttu-id="1e11e-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1e11e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e11e-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e11e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e11e-142">CommonParameters</span></span>
<span data-ttu-id="1e11e-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e11e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e11e-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1e11e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e11e-145">입력</span><span class="sxs-lookup"><span data-stu-id="1e11e-145">INPUTS</span></span>

### <span data-ttu-id="1e11e-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1e11e-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1e11e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="1e11e-147">System.String</span></span>

### <span data-ttu-id="1e11e-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1e11e-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="1e11e-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1e11e-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="1e11e-150">출력</span><span class="sxs-lookup"><span data-stu-id="1e11e-150">OUTPUTS</span></span>

### <span data-ttu-id="1e11e-151">System.Void</span><span class="sxs-lookup"><span data-stu-id="1e11e-151">System.Void</span></span>

## <span data-ttu-id="1e11e-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1e11e-152">NOTES</span></span>

## <span data-ttu-id="1e11e-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e11e-153">RELATED LINKS</span></span>
