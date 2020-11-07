---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: 94fbc71db34ca0abc6a27130dc166318794e271a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698303"
---
# <span data-ttu-id="c2139-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c2139-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="c2139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2139-102">SYNOPSIS</span></span>

## <span data-ttu-id="c2139-103">구문과</span><span class="sxs-lookup"><span data-stu-id="c2139-103">SYNTAX</span></span>

### <span data-ttu-id="c2139-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c2139-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="c2139-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c2139-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="c2139-106">설명은</span><span class="sxs-lookup"><span data-stu-id="c2139-106">DESCRIPTION</span></span>
<span data-ttu-id="c2139-107">**Restore-AzWebAppBackup** Cmdlet은 Azure Web App 백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2139-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="c2139-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c2139-108">EXAMPLES</span></span>

### <span data-ttu-id="c2139-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="c2139-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="c2139-110">리소스 그룹 Default-WestUS 내에 있는 지정 된 앱 ContosoWebApp의 백업을 다음 위치의 blob "myBlob"에 복원 합니다. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="c2139-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="c2139-111">변수</span><span class="sxs-lookup"><span data-stu-id="c2139-111">PARAMETERS</span></span>

### <span data-ttu-id="c2139-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c2139-112">-AppServicePlan</span></span>
<span data-ttu-id="c2139-113">복원 된 앱에 대 한 앱 서비스 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2139-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="c2139-114">이 옵션을 비워 두면 앱의 현재 앱 서비스 계획이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2139-114">If left empty, the app's current App Service Plan is used.</span></span>

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

### <span data-ttu-id="c2139-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="c2139-115">-BlobName</span></span>
<span data-ttu-id="c2139-116">Blob 이름</span><span class="sxs-lookup"><span data-stu-id="c2139-116">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2139-117">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="c2139-117">-Databases</span></span>
<span data-ttu-id="c2139-118">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="c2139-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2139-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2139-119">-DefaultProfile</span></span>
<span data-ttu-id="c2139-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2139-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2139-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="c2139-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="c2139-122">충돌 하는 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="c2139-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="c2139-123">-이름</span><span class="sxs-lookup"><span data-stu-id="c2139-123">-Name</span></span>
<span data-ttu-id="c2139-124">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="c2139-124">WebApp Name</span></span>

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

### <span data-ttu-id="c2139-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="c2139-125">-Overwrite</span></span>
<span data-ttu-id="c2139-126">덮어쓰기 옵션</span><span class="sxs-lookup"><span data-stu-id="c2139-126">Overwrite Option</span></span>

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

### <span data-ttu-id="c2139-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2139-127">-ResourceGroupName</span></span>
<span data-ttu-id="c2139-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c2139-128">Resource Group Name</span></span>

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

### <span data-ttu-id="c2139-129">-슬롯</span><span class="sxs-lookup"><span data-stu-id="c2139-129">-Slot</span></span>
<span data-ttu-id="c2139-130">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="c2139-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c2139-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="c2139-131">-StorageAccountUrl</span></span>
<span data-ttu-id="c2139-132">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="c2139-132">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2139-133">-Web app</span><span class="sxs-lookup"><span data-stu-id="c2139-133">-WebApp</span></span>
<span data-ttu-id="c2139-134">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="c2139-134">WebApp Object</span></span>

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

### <span data-ttu-id="c2139-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2139-135">CommonParameters</span></span>
<span data-ttu-id="c2139-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2139-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2139-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2139-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2139-138">입력</span><span class="sxs-lookup"><span data-stu-id="c2139-138">INPUTS</span></span>

### <span data-ttu-id="c2139-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2139-139">System.String</span></span>

### <span data-ttu-id="c2139-140">DatabaseBackupSetting [] (으)로</span><span class="sxs-lookup"><span data-stu-id="c2139-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="c2139-141">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2139-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c2139-142">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="c2139-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c2139-143">출력</span><span class="sxs-lookup"><span data-stu-id="c2139-143">OUTPUTS</span></span>

### <span data-ttu-id="c2139-144">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="c2139-144">System.Void</span></span>

## <span data-ttu-id="c2139-145">상속자</span><span class="sxs-lookup"><span data-stu-id="c2139-145">NOTES</span></span>

## <span data-ttu-id="c2139-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2139-146">RELATED LINKS</span></span>