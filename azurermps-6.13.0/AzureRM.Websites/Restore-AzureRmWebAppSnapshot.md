---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 536d0fe0f32231bfd732698c584e02be95d5c20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529307"
---
# <span data-ttu-id="6e11e-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="6e11e-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="6e11e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e11e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e11e-103">웹 앱 스냅숏을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e11e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e11e-104">SYNTAX</span></span>

### <span data-ttu-id="6e11e-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6e11e-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e11e-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6e11e-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e11e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6e11e-107">DESCRIPTION</span></span>
<span data-ttu-id="6e11e-108">웹 앱 스냅숏을 웹 앱으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="6e11e-109">스냅숏을 복원 하면 웹 앱의 모든 파일을 스냅숏에 포함 된 파일로 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="6e11e-110">설정도 복원 하려면 RecoverConfiguration switch 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="6e11e-111">한 웹 앱의 스냅숏을 동일한 구독에서 다른 웹 앱으로 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="6e11e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="6e11e-112">EXAMPLES</span></span>

### <span data-ttu-id="6e11e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e11e-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="6e11e-114">"Default-WestUS" 리소스 그룹에서 "Staging" 이라는 슬롯이 있는 "ContosoApp" 라는 웹 앱의 최신 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="6e11e-115">스냅샷을 웹 앱의 "복원" 슬롯으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="6e11e-116">변수</span><span class="sxs-lookup"><span data-stu-id="6e11e-116">PARAMETERS</span></span>

### <span data-ttu-id="6e11e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e11e-117">-AsJob</span></span>
<span data-ttu-id="6e11e-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6e11e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e11e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e11e-119">-DefaultProfile</span></span>
<span data-ttu-id="6e11e-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e11e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6e11e-121">-Force</span></span>
<span data-ttu-id="6e11e-122">원본 웹 앱을 덮어쓸 수 있도록 경고를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="6e11e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e11e-123">-InputObject</span></span>
<span data-ttu-id="6e11e-124">Azure Web App 스냅숏입니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="6e11e-125">-이름</span><span class="sxs-lookup"><span data-stu-id="6e11e-125">-Name</span></span>
<span data-ttu-id="6e11e-126">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-126">The name of the web app.</span></span>

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

### <span data-ttu-id="6e11e-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e11e-127">-RecoverConfiguration</span></span>
<span data-ttu-id="6e11e-128">파일 외에 웹 앱의 구성을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="6e11e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e11e-129">-ResourceGroupName</span></span>
<span data-ttu-id="6e11e-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="6e11e-131">-슬롯</span><span class="sxs-lookup"><span data-stu-id="6e11e-131">-Slot</span></span>
<span data-ttu-id="6e11e-132">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="6e11e-133">-Web app</span><span class="sxs-lookup"><span data-stu-id="6e11e-133">-WebApp</span></span>
<span data-ttu-id="6e11e-134">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="6e11e-134">The web app object</span></span>

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

### <span data-ttu-id="6e11e-135">-확인</span><span class="sxs-lookup"><span data-stu-id="6e11e-135">-Confirm</span></span>
<span data-ttu-id="6e11e-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e11e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e11e-137">-WhatIf</span></span>
<span data-ttu-id="6e11e-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e11e-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e11e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e11e-140">CommonParameters</span></span>
<span data-ttu-id="6e11e-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e11e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e11e-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e11e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e11e-143">입력</span><span class="sxs-lookup"><span data-stu-id="6e11e-143">INPUTS</span></span>

### <span data-ttu-id="6e11e-144">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6e11e-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6e11e-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6e11e-145">System.String</span></span>

### <span data-ttu-id="6e11e-146">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="6e11e-146">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="6e11e-147">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e11e-147">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="6e11e-148">AzureWebAppSnapshot (\*). i m App.</span><span class="sxs-lookup"><span data-stu-id="6e11e-148">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>
<span data-ttu-id="6e11e-149">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e11e-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6e11e-150">출력</span><span class="sxs-lookup"><span data-stu-id="6e11e-150">OUTPUTS</span></span>

### <span data-ttu-id="6e11e-151">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="6e11e-151">System.Void</span></span>

## <span data-ttu-id="6e11e-152">상속자</span><span class="sxs-lookup"><span data-stu-id="6e11e-152">NOTES</span></span>

## <span data-ttu-id="6e11e-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e11e-153">RELATED LINKS</span></span>
