---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: d7fd26d81b683095fb08c1dbca3226761f047d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529057"
---
# <span data-ttu-id="7d54f-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d54f-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="7d54f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d54f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d54f-103">구문과</span><span class="sxs-lookup"><span data-stu-id="7d54f-103">SYNTAX</span></span>

### <span data-ttu-id="7d54f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7d54f-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="7d54f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7d54f-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="7d54f-106">설명은</span><span class="sxs-lookup"><span data-stu-id="7d54f-106">DESCRIPTION</span></span>
<span data-ttu-id="7d54f-107">**편집-AzureRmWebAppBackupConfiguration** Cmdlet은 Azure Web App에 대 한 현재 구성 백업을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d54f-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="7d54f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7d54f-108">EXAMPLES</span></span>

## <span data-ttu-id="7d54f-109">변수</span><span class="sxs-lookup"><span data-stu-id="7d54f-109">PARAMETERS</span></span>

### <span data-ttu-id="7d54f-110">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="7d54f-110">-Databases</span></span>
<span data-ttu-id="7d54f-111">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="7d54f-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d54f-112">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="7d54f-112">-FrequencyInterval</span></span>
<span data-ttu-id="7d54f-113">빈도 간격</span><span class="sxs-lookup"><span data-stu-id="7d54f-113">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d54f-114">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="7d54f-114">-FrequencyUnit</span></span>
<span data-ttu-id="7d54f-115">주파수 단위</span><span class="sxs-lookup"><span data-stu-id="7d54f-115">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d54f-116">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="7d54f-116">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="7d54f-117">하나 이상의 백업 옵션 유지</span><span class="sxs-lookup"><span data-stu-id="7d54f-117">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d54f-118">-이름</span><span class="sxs-lookup"><span data-stu-id="7d54f-118">-Name</span></span>
<span data-ttu-id="7d54f-119">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="7d54f-119">WebApp Name</span></span>

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

### <span data-ttu-id="7d54f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d54f-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d54f-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7d54f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="7d54f-122">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="7d54f-122">-RetentionPeriodInDays</span></span>
<span data-ttu-id="7d54f-123">보존 기간 (일)</span><span class="sxs-lookup"><span data-stu-id="7d54f-123">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d54f-124">-슬롯</span><span class="sxs-lookup"><span data-stu-id="7d54f-124">-Slot</span></span>
<span data-ttu-id="7d54f-125">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="7d54f-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7d54f-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7d54f-126">-StartTime</span></span>
<span data-ttu-id="7d54f-127">UTC의 StartTime</span><span class="sxs-lookup"><span data-stu-id="7d54f-127">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d54f-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="7d54f-128">-StorageAccountUrl</span></span>
<span data-ttu-id="7d54f-129">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="7d54f-129">Storage Account Url</span></span>

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

### <span data-ttu-id="7d54f-130">-Web app</span><span class="sxs-lookup"><span data-stu-id="7d54f-130">-WebApp</span></span>
<span data-ttu-id="7d54f-131">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="7d54f-131">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d54f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d54f-132">-DefaultProfile</span></span>
<span data-ttu-id="7d54f-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d54f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d54f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d54f-134">CommonParameters</span></span>
<span data-ttu-id="7d54f-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d54f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d54f-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d54f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d54f-137">입력</span><span class="sxs-lookup"><span data-stu-id="7d54f-137">INPUTS</span></span>

### <span data-ttu-id="7d54f-138">Site</span><span class="sxs-lookup"><span data-stu-id="7d54f-138">Site</span></span>
<span data-ttu-id="7d54f-139">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d54f-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7d54f-140">출력</span><span class="sxs-lookup"><span data-stu-id="7d54f-140">OUTPUTS</span></span>

### <span data-ttu-id="7d54f-141">AzureWebAppBackupConfiguration (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="7d54f-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="7d54f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="7d54f-142">NOTES</span></span>

## <span data-ttu-id="7d54f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d54f-143">RELATED LINKS</span></span>

[<span data-ttu-id="7d54f-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d54f-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


