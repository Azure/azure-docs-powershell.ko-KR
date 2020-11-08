---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 8C7551CD-0222-44D1-AA1B-647669B01853
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdb7b8f1b53f7352e3e147c6f203e3a4460e8a05
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046289"
---
# <span data-ttu-id="0b624-101">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0b624-101">Get-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="0b624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b624-102">SYNOPSIS</span></span>
<span data-ttu-id="0b624-103">백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-103">Gets backup policies.</span></span>

## <span data-ttu-id="0b624-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b624-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> [-BackupPolicyName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0b624-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b624-105">DESCRIPTION</span></span>
<span data-ttu-id="0b624-106">**Get-AzureStorSimpleDeviceBackupPolicy** cmdlet은 백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-106">The **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet gets backup policies.</span></span>
<span data-ttu-id="0b624-107">이 cmdlet은 **백업 정책** 개체 또는 장치에 속하는 모든 **backuppolicy** 개체의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-107">This cmdlet returns a **BackupPolicy** object or a list of all the **BackupPolicy** objects that belong to a device.</span></span>
<span data-ttu-id="0b624-108">백업 정책 개체에는 다음 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-108">The backup policy objects contain the following properties:</span></span> 

- <span data-ttu-id="0b624-109">**성을**</span><span class="sxs-lookup"><span data-stu-id="0b624-109">**Name**</span></span>
- <span data-ttu-id="0b624-110">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="0b624-110">**InstanceId**</span></span>
- <span data-ttu-id="0b624-111">**BackupPolicyCreationType**</span><span class="sxs-lookup"><span data-stu-id="0b624-111">**BackupPolicyCreationType**</span></span>
- <span data-ttu-id="0b624-112">**마지막 백업**</span><span class="sxs-lookup"><span data-stu-id="0b624-112">**LastBackup**</span></span>
- <span data-ttu-id="0b624-113">**NextBackup**</span><span class="sxs-lookup"><span data-stu-id="0b624-113">**NextBackup**</span></span>
- <span data-ttu-id="0b624-114">**SchedulesCount**</span><span class="sxs-lookup"><span data-stu-id="0b624-114">**SchedulesCount**</span></span>
- <span data-ttu-id="0b624-115">**SSMHostName**</span><span class="sxs-lookup"><span data-stu-id="0b624-115">**SSMHostName**</span></span>
- <span data-ttu-id="0b624-116">**(는) Escount**</span><span class="sxs-lookup"><span data-stu-id="0b624-116">**VolumesCount**</span></span>

## <span data-ttu-id="0b624-117">예제의</span><span class="sxs-lookup"><span data-stu-id="0b624-117">EXAMPLES</span></span>

### <span data-ttu-id="0b624-118">예제 1: 정책에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0b624-118">Example 1: Get details for a policy</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralBackupPolicy07"
VERBOSE: ClientRequestId: 2a878cd6-8432-4646-8be8-a0cb0750958e_PS
VERBOSE: ClientRequestId: 00ea5a6d-8c27-4e22-b182-5969cdbb8033_PS
VERBOSE: ClientRequestId: 39dac9ff-4455-45ae-ae3d-7de1445b9520_PS


BackupSchedules          : {8658e3a2-8a59-4d43-8725-ab0c95665301}
Volumes                  : {testvolume03, testvolume05}
BackupPolicyCreationType : BySaaS
LastBackup               : 
NextBackup               : 16-12-2014 00:30:00
SchedulesCount           : 1
SSMHostName              : 
VolumesCount             : 2
InstanceId               : 84140a6a-9254-4fff-8d09-ae40e9f1bc7d
Name                     : GeneralBackupPolicy07
OperationInProgress      : None

VERBOSE: BackupPolicy with id 84140a6a-9254-4fff-8d09-ae40e9f1bc7d found!
```

<span data-ttu-id="0b624-119">이 명령은 Contoso63-AppVm 이라는 장치에서 GeneralBackupPolicy07 라는 **Backuppolicydetails** 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-119">This command gets a **BackupPolicyDetails** object named GeneralBackupPolicy07 on the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="0b624-120">예제 2: 백업 정책 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="0b624-120">Example 2: Get a list of backup policies</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               SchedulesCount VolumesCount                       BackupPolicyCreationType          LastBackup                        NextBackup                        SSMHostName                      
----------                           ----                               -------------- ------------                       ------------------------          ----------                        ----------                        -----------                      
13db29a4-bba9-4871-b872-db1fa0506b16 VG Clones                          1              2                                  BySaaS                            4/15/2015 8:30:02 AM              4/15/2015 8:30:00 PM                                               
2dcd3002-13c4-4bdb-a1ef-b35ce0a29416 vg-all                             1              4                                  BySaaS                            3/27/2015 9:12:15 PM              1/1/2010 5:30:00 AM                                                
54828d08-8309-4bd4-828f-21904863fb4c Cloud_Snapshot_Vol3_clone VG       1              1                                  BySaaS                            4/15/2015 9:00:03 AM              4/17/2015 9:00:30 AM                                               
6a51f39e-0ec9-4c57-8ec9-14a9255efa95 Test Group                         0              2                                  BySaaS                            3/27/2015 1:47:00 AM              1/1/2010 5:30:00 AM                                                
81c2db43-38f7-45fc-b2f2-476d1f6039a7 Cloud_Snapshot_Vol1_clone VG       1              1                                  BySaaS                            4/15/2015 7:30:02 AM              4/17/2015 7:30:00 AM                                               
82c4a5be-7473-431f-86e7-9db31ee9a9f8 Cloud_Snapshot_vg-all              1              4                                  BySaaS                            4/15/2015 11:30:02 AM             4/15/2015 3:30:00 PM                                               
cda96e83-3b38-4345-a56d-c8a96a0e57b3 Snapshot_vg-all                    1              4                                  BySaaS                            4/15/2015 1:30:02 PM              4/15/2015 3:30:00 PM
```

<span data-ttu-id="0b624-121">이 명령은 Contoso63 이라는 디바이스의 **Backuppolicy** 개체를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-121">This command lists the **BackupPolicy** objects on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="0b624-122">변수</span><span class="sxs-lookup"><span data-stu-id="0b624-122">PARAMETERS</span></span>

### <span data-ttu-id="0b624-123">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="0b624-123">-BackupPolicyName</span></span>
<span data-ttu-id="0b624-124">가져올 백업 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-124">Specifies the name of the backup policy to get.</span></span>
<span data-ttu-id="0b624-125">이 매개 변수를 지정 하지 않으면이 cmdlet은 모든 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-125">If you do not specify this parameter, this cmdlet gets all policies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b624-126">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="0b624-126">-DeviceName</span></span>
<span data-ttu-id="0b624-127">백업 정책을 만들 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-127">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b624-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="0b624-128">-Profile</span></span>
<span data-ttu-id="0b624-129">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-129">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b624-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b624-130">CommonParameters</span></span>
<span data-ttu-id="0b624-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b624-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b624-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b624-133">입력</span><span class="sxs-lookup"><span data-stu-id="0b624-133">INPUTS</span></span>

### <span data-ttu-id="0b624-134">않아야</span><span class="sxs-lookup"><span data-stu-id="0b624-134">None</span></span>

## <span data-ttu-id="0b624-135">출력</span><span class="sxs-lookup"><span data-stu-id="0b624-135">OUTPUTS</span></span>

### <span data-ttu-id="0b624-136">IList \<BackupPolicy\> , backuppolicydetails</span><span class="sxs-lookup"><span data-stu-id="0b624-136">IList\<BackupPolicy\>, BackupPolicyDetails</span></span>
<span data-ttu-id="0b624-137">*BackupPolicyName* 매개 변수를 지정 하는 경우이 Cmdlet은 **backuppolicydetails** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-137">This cmdlet returns a **BackupPolicyDetails** object, if you specify the *BackupPolicyName* parameter.</span></span>
<span data-ttu-id="0b624-138">해당 매개 변수를 지정 하지 않으면 **IList \<BackupPolicy\>** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b624-138">If you do not specify that parameter, it returns an **IList\<BackupPolicy\>** object.</span></span>

## <span data-ttu-id="0b624-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0b624-139">NOTES</span></span>

## <span data-ttu-id="0b624-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b624-140">RELATED LINKS</span></span>

[<span data-ttu-id="0b624-141">새로운 AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0b624-141">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="0b624-142">제거-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0b624-142">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="0b624-143">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0b624-143">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


