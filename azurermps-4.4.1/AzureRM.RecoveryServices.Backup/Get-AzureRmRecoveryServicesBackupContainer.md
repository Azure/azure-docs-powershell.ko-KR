---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: e6b0633b43bc93c516c9c5b6f4872ecbd6d68520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711253"
---
# <span data-ttu-id="89af7-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="89af7-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="89af7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89af7-102">SYNOPSIS</span></span>
<span data-ttu-id="89af7-103">백업 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89af7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89af7-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89af7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89af7-105">DESCRIPTION</span></span>
<span data-ttu-id="89af7-106">**Get-AzureRmRecoveryServicesBackupContainer** cmdlet은 백업 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="89af7-107">백업 컨테이너는 백업 항목으로 modelled 된 데이터 원본을 캡슐화 합니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>

<span data-ttu-id="89af7-108">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="89af7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="89af7-109">EXAMPLES</span></span>

### <span data-ttu-id="89af7-110">예제 1: 특정 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="89af7-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="89af7-111">이 명령은 Add-azurevm 유형의 V2VM 이라는 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="89af7-112">예제 2: 특정 형식의 모든 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="89af7-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="89af7-113">이 명령은 Azure Backup agent로 보호 되는 모든 Windows 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="89af7-114">*Backupmanagementtype* 매개 변수는 Windows 컨테이너에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="89af7-115">변수</span><span class="sxs-lookup"><span data-stu-id="89af7-115">PARAMETERS</span></span>

### <span data-ttu-id="89af7-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="89af7-116">-BackupManagementType</span></span>
<span data-ttu-id="89af7-117">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-117">Specifies the backup management type.</span></span>
<span data-ttu-id="89af7-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89af7-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="89af7-119">AzureVM</span></span>
- <span data-ttu-id="89af7-120">화성</span><span class="sxs-lookup"><span data-stu-id="89af7-120">MARS</span></span>
- <span data-ttu-id="89af7-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="89af7-121">AzureSQL</span></span>

<span data-ttu-id="89af7-122">이 매개 변수는 MARS 에이전트 또는 다른 백업 엔진을 사용 하 여 백업 되는 Windows 컴퓨터를 구분 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-122">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89af7-123">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="89af7-123">-ContainerType</span></span>
<span data-ttu-id="89af7-124">백업 컨테이너 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-124">Specifies the backup container type.</span></span>
<span data-ttu-id="89af7-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89af7-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="89af7-126">AzureVM</span></span> 
- <span data-ttu-id="89af7-127">창을</span><span class="sxs-lookup"><span data-stu-id="89af7-127">Windows</span></span>
- <span data-ttu-id="89af7-128">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="89af7-128">AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89af7-129">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="89af7-129">-FriendlyName</span></span>
<span data-ttu-id="89af7-130">가져올 컨테이너의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-130">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89af7-131">-이름</span><span class="sxs-lookup"><span data-stu-id="89af7-131">-Name</span></span>
<span data-ttu-id="89af7-132">가져올 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-132">Specifies the name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89af7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89af7-133">-ResourceGroupName</span></span>
<span data-ttu-id="89af7-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="89af7-135">이 매개 변수는 Azure 가상 머신에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-135">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89af7-136">-상태</span><span class="sxs-lookup"><span data-stu-id="89af7-136">-Status</span></span>
<span data-ttu-id="89af7-137">컨테이너 등록 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-137">Specifies the container registration status.</span></span>
<span data-ttu-id="89af7-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89af7-139">되어</span><span class="sxs-lookup"><span data-stu-id="89af7-139">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89af7-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89af7-140">-DefaultProfile</span></span>
<span data-ttu-id="89af7-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89af7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89af7-142">CommonParameters</span></span>
<span data-ttu-id="89af7-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89af7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89af7-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89af7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89af7-145">입력</span><span class="sxs-lookup"><span data-stu-id="89af7-145">INPUTS</span></span>

## <span data-ttu-id="89af7-146">출력</span><span class="sxs-lookup"><span data-stu-id="89af7-146">OUTPUTS</span></span>

### <span data-ttu-id="89af7-147">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="89af7-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="89af7-148">System.webserver. IList ' 1 [Microsoft Azure. e. ContainerBase]을 (를)</span><span class="sxs-lookup"><span data-stu-id="89af7-148">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase]</span></span>

## <span data-ttu-id="89af7-149">상속자</span><span class="sxs-lookup"><span data-stu-id="89af7-149">NOTES</span></span>

## <span data-ttu-id="89af7-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89af7-150">RELATED LINKS</span></span>

[<span data-ttu-id="89af7-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="89af7-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="89af7-152">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="89af7-152">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="89af7-153">등록 취소-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="89af7-153">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


