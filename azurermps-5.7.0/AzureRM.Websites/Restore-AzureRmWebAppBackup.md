---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: c68d9afb7c9498bbf734abcc376e6f123ebb8ac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533516"
---
# <span data-ttu-id="df88d-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="df88d-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="df88d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df88d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df88d-103">구문과</span><span class="sxs-lookup"><span data-stu-id="df88d-103">SYNTAX</span></span>

### <span data-ttu-id="df88d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="df88d-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="df88d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="df88d-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="df88d-106">설명은</span><span class="sxs-lookup"><span data-stu-id="df88d-106">DESCRIPTION</span></span>
<span data-ttu-id="df88d-107">**Restore-AzureRmWebAppBackup** Cmdlet은 Azure Web App 백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="df88d-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="df88d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="df88d-108">EXAMPLES</span></span>

### <span data-ttu-id="df88d-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="df88d-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="df88d-110">리소스 그룹 Default-WestUS 내에 있는 지정 된 앱 ContosoWebApp의 백업을 다음 위치의 blob "myBlob"에 복원 합니다. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="df88d-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="df88d-111">변수</span><span class="sxs-lookup"><span data-stu-id="df88d-111">PARAMETERS</span></span>

### <span data-ttu-id="df88d-112">-BlobName</span><span class="sxs-lookup"><span data-stu-id="df88d-112">-BlobName</span></span>
<span data-ttu-id="df88d-113">Blob 이름</span><span class="sxs-lookup"><span data-stu-id="df88d-113">Blob Name</span></span>

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

### <span data-ttu-id="df88d-114">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="df88d-114">-Databases</span></span>
<span data-ttu-id="df88d-115">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="df88d-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="df88d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df88d-116">-DefaultProfile</span></span>
<span data-ttu-id="df88d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df88d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df88d-118">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="df88d-118">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="df88d-119">충돌 하는 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="df88d-119">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="df88d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="df88d-120">-Name</span></span>
<span data-ttu-id="df88d-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="df88d-121">WebApp Name</span></span>

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

### <span data-ttu-id="df88d-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="df88d-122">-Overwrite</span></span>
<span data-ttu-id="df88d-123">덮어쓰기 옵션</span><span class="sxs-lookup"><span data-stu-id="df88d-123">Overwrite Option</span></span>

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

### <span data-ttu-id="df88d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df88d-124">-ResourceGroupName</span></span>
<span data-ttu-id="df88d-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="df88d-125">Resource Group Name</span></span>

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

### <span data-ttu-id="df88d-126">-슬롯</span><span class="sxs-lookup"><span data-stu-id="df88d-126">-Slot</span></span>
<span data-ttu-id="df88d-127">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="df88d-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="df88d-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="df88d-128">-StorageAccountUrl</span></span>
<span data-ttu-id="df88d-129">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="df88d-129">Storage Account Url</span></span>

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

### <span data-ttu-id="df88d-130">-Web app</span><span class="sxs-lookup"><span data-stu-id="df88d-130">-WebApp</span></span>
<span data-ttu-id="df88d-131">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="df88d-131">WebApp Object</span></span>

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

### <span data-ttu-id="df88d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df88d-132">CommonParameters</span></span>
<span data-ttu-id="df88d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="df88d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df88d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df88d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df88d-135">입력</span><span class="sxs-lookup"><span data-stu-id="df88d-135">INPUTS</span></span>

### <span data-ttu-id="df88d-136">Site</span><span class="sxs-lookup"><span data-stu-id="df88d-136">Site</span></span>
<span data-ttu-id="df88d-137">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="df88d-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="df88d-138">출력</span><span class="sxs-lookup"><span data-stu-id="df88d-138">OUTPUTS</span></span>

## <span data-ttu-id="df88d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="df88d-139">NOTES</span></span>

## <span data-ttu-id="df88d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df88d-140">RELATED LINKS</span></span>

