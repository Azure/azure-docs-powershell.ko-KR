---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 9c28d9235eefe6c4f33537115b548137c5bc6c88
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882434"
---
# <span data-ttu-id="e0ddd-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e0ddd-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="e0ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0ddd-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0ddd-103">구문과</span><span class="sxs-lookup"><span data-stu-id="e0ddd-103">SYNTAX</span></span>

### <span data-ttu-id="e0ddd-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e0ddd-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="e0ddd-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e0ddd-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="e0ddd-106">설명은</span><span class="sxs-lookup"><span data-stu-id="e0ddd-106">DESCRIPTION</span></span>
<span data-ttu-id="e0ddd-107">**Restore-AzureRmWebAppBackup** Cmdlet은 Azure Web App 백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0ddd-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="e0ddd-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e0ddd-108">EXAMPLES</span></span>

### <span data-ttu-id="e0ddd-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="e0ddd-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="e0ddd-110">리소스 그룹 Default-WestUS 내에 있는 지정 된 앱 ContosoWebApp의 백업을 다음 위치의 blob "myBlob"에 복원 합니다. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="e0ddd-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="e0ddd-111">변수</span><span class="sxs-lookup"><span data-stu-id="e0ddd-111">PARAMETERS</span></span>

### <span data-ttu-id="e0ddd-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e0ddd-112">-AppServicePlan</span></span>
<span data-ttu-id="e0ddd-113">복원 된 앱에 대 한 앱 서비스 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0ddd-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="e0ddd-114">이 옵션을 비워 두면 앱의 현재 앱 서비스 계획이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0ddd-114">If left empty, the app's current App Service Plan is used.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="e0ddd-115">-BlobName</span></span>
<span data-ttu-id="e0ddd-116">Blob 이름</span><span class="sxs-lookup"><span data-stu-id="e0ddd-116">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-117">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="e0ddd-117">-Databases</span></span>
<span data-ttu-id="e0ddd-118">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="e0ddd-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ddd-119">-DefaultProfile</span></span>
<span data-ttu-id="e0ddd-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0ddd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="e0ddd-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="e0ddd-122">충돌 하는 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="e0ddd-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-123">-이름</span><span class="sxs-lookup"><span data-stu-id="e0ddd-123">-Name</span></span>
<span data-ttu-id="e0ddd-124">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="e0ddd-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e0ddd-125">-Overwrite</span></span>
<span data-ttu-id="e0ddd-126">덮어쓰기 옵션</span><span class="sxs-lookup"><span data-stu-id="e0ddd-126">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ddd-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0ddd-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e0ddd-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-129">-슬롯</span><span class="sxs-lookup"><span data-stu-id="e0ddd-129">-Slot</span></span>
<span data-ttu-id="e0ddd-130">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="e0ddd-130">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="e0ddd-131">-StorageAccountUrl</span></span>
<span data-ttu-id="e0ddd-132">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="e0ddd-132">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-133">-Web app</span><span class="sxs-lookup"><span data-stu-id="e0ddd-133">-WebApp</span></span>
<span data-ttu-id="e0ddd-134">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="e0ddd-134">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ddd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ddd-135">CommonParameters</span></span>
<span data-ttu-id="e0ddd-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0ddd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ddd-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ddd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ddd-138">입력</span><span class="sxs-lookup"><span data-stu-id="e0ddd-138">INPUTS</span></span>

### <span data-ttu-id="e0ddd-139">Site</span><span class="sxs-lookup"><span data-stu-id="e0ddd-139">Site</span></span>
<span data-ttu-id="e0ddd-140">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0ddd-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e0ddd-141">출력</span><span class="sxs-lookup"><span data-stu-id="e0ddd-141">OUTPUTS</span></span>

## <span data-ttu-id="e0ddd-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e0ddd-142">NOTES</span></span>

## <span data-ttu-id="e0ddd-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0ddd-143">RELATED LINKS</span></span>

