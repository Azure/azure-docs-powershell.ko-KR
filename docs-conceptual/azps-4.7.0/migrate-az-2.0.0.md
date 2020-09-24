---
title: Az 2.0.0 마이그레이션 가이드
description: 이 마이그레이션 가이드에는 Az 버전 2.0 릴리스의 Azure PowerShell에 대한 호환성이 손상되는 변경 목록이 나와 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2d8a3c04388bfc5028811f6d1b6caf2c6fce4147
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928172"
---
# <a name="migration-guide-for-az-200"></a>Az 2.0.0 마이그레이션 가이드

이 문서에서는 Az 1.0.0 및 2.0.0 버전 간의 변경 내용에 대해 설명합니다. 

## <a name="table-of-contents"></a>목차
- [모듈의 호환성이 손상되는 변경](#module-breaking-changes)
  - [Az.Compute](#azcompute)
  - [Az.HDInsight](#azhdinsight)
  - [Az.Storage](#azstorage)

## <a name="module-breaking-changes"></a>모듈의 호환성이 손상되는 변경

### <a name="azcompute"></a>Az.Compute

- ```Sku = Aligned```를 사용하기 위해 `New-AzAvailabilitySet` 및 `Update-AzAvailabilitySet` cmdlet에서 `Managed` 매개 변수를 제거했습니다.

  #### <a name="before"></a>이전

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a>After

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- 일관성을 위해 `Update-AzImage`의 'ByName' 및 'ByResourceId' 매개 변수 집합에서 `Image` 매개 변수를 제거했습니다. 
  
  #### <a name="before"></a>이전

  아래 코드는 작동하지만, 전달된 ImageName은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a>After

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- 일관성을 위해 `Restart-AzVM`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.
  
  #### <a name="before"></a>이전

  아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- 일관성을 위해 `Start-AzVM`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.
  
  #### <a name="before"></a>이전

  아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- 일관성을 위해 `Stop-AzVM`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.
  
  #### <a name="before"></a>이전

  아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- 일관성을 위해 `Remove-AzVM`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.
  
  #### <a name="before"></a>이전

  아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a>After

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- 일관성을 위해 `Set-AzVM`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다.
  
  #### <a name="before"></a>이전

  아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- 일관성을 위해 `Save-AzVMImage`의 'ByObject' 및 'ByResourceId' 매개 변수 집합에서 `Name` 매개 변수를 제거했습니다. 
  
  #### <a name="before"></a>이전
  아래 코드는 작동하지만, 전달된 Name은 사용되지 않으므로 이 매개 변수를 제거해도 기능에는 아무런 영향을 주지 않습니다.
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a>After
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- `PSVirtualMachineScaleSetVM`의 `ProtectFromScaleIn` 속성을 캡슐화하기 위해 ProtectionPolicy 속성을 추가했습니다.

  #### <a name="before"></a>이전

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a>After

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- `PSDisk`의 `EncryptionSettings` 속성을 묶기 위해 ```EncryptionSettingsCollection``` 속성을 추가했습니다.

  #### <a name="before"></a>이전

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>After

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- `PSSnapshot`의 `EncryptionSettings` 속성을 묶기 위해 ```EncryptionSettingsCollection``` 속성을 추가했습니다.

  #### <a name="before"></a>이전

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>After

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- `PSVirtualMachineScaleSet`에서 `VirtualMachineProfile` 속성을 제거했습니다.

  #### <a name="before"></a>이전

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a>After

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- `Set-AzVMBootDiagnostic` cmdlet에서 `Set-AzVMBootDiagnostics`에 대한 별칭을 제거했습니다.

  #### <a name="before"></a>이전

  사용되지 않는 별칭을 사용했습니다.

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- `Export-AzLogAnalyticThrottledRequest` cmdlet에서 `Export-AzLogAnalyticThrottledRequests`에 대한 별칭을 제거했습니다.

  #### <a name="before"></a>이전

  사용되지 않는 별칭을 사용했습니다.

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a>After

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a>Az.HDInsight

- `Grant-AzHDInsightHttpServicesAccess` 및 `Revoke-AzHDInsightHttpServicesAccess` cmdlet을 제거했습니다. HTTP 액세스는 모든 HDInsight 클러스터에서 항상 사용하도록 설정되므로 더 이상 필요하지 않습니다.
- 새 `Set-AzHDInsightGatewayCredential` cmdlet을 추가했습니다. 이 cmdlet을 사용하여 게이트웨이 HTTP 사용자 이름 및 암호를 변경합니다(`Grant-AzHDInsightHttpServicesAccess` 대체).
- 스토리지 키에 대한 세분화된 역할 기반 액세스를 지원하도록 `Get-AzHDInsightJobOutput` cmdlet을 업데이트했습니다.
    - HDInsight 클러스터 운영자, 기여자 또는 소유자 역할이 있는 사용자는 영향을 받지 않습니다.
    - 읽기 권한자 역할만 있는 사용자는 `DefaultStorageAccountKey` 매개 변수를 명시적으로 지정해야 합니다.

이러한 역할 기반 액세스 변경에 대한 자세한 내용은 [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)를 참조하세요.

  #### <a name="before"></a>이전

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a>Get-AzHDInsightJobOutput cmdlet에 대한 읽기 권한자 역할만 있는 사용자

  ####  <a name="before"></a>이전

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a>After

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a>Az.Storage

- Blob, Queue 및 File cmdlet에서 반환된 형식의 네임스페이스를 `Microsoft.WindowsAzure.Storage`에서 `Microsoft.Azure.Storage`로 변경했습니다.  이는 기술적으로 호환성이 손상되는 변경 정책에 따른 호환성이 손상되는 변경이 아니지만, 이러한 cmdlet에서 반환되는 개체와 상호 작용하기 위해 Storage .Net SDK의 메서드를 사용하는 코드를 일부 변경해야 할 수 있습니다.

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a>예제 1:  Queue에 메시지 추가(CloudQueueMessage 개체 네임스페이스 변경)

  이전: 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  이후:

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a>예제 2:  AccessCondition을 사용하여 Blob/File 특성 가져오기(AccessCondition 개체 네임스페이스 변경)

  이전: 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  이후:

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- 기술적으로 호환성이 손상되는 변경이 아니지만, `New/Get/Set-AzStorageAccount` 변경에서 반환되는 스토리지 계정의 Sku.Name 속성의 출력 차이가 다음과 같습니다. (변경되면 출력 및 입력 SkuName이 정렬됩니다.)
  - "StandardLRS" -> "Standard_LRS"
  - "StandardGRS" -> "Standard_GRS"
  - "StandardRAGRS" -> "Standard_RAGRS"
  - "StandardZRS" -> "Standard_ZRS"
  - "PremiumLRS" -> "Premium_LRS"

- Kind를 지정하지 않고 스토리지 계정을 만들 때의 기본 서비스 동작을 변경했습니다.  이전 버전에서는 `Kind`가 지정되지 않은 스토리지 계정을 만들 때 `Storage`라는 스토리지 계정 종류가 사용되었지만, 새 `StorageV2` 버전에서 기본값은 `Kind`입니다. Kind 'Storage'를 사용하여 V1 스토리지 계정을 만들어야 하는 경우 '-Kind Storage' 매개 변수를 추가합니다.

  #### <a name="example--create-a-storage-account-default-kind-change"></a>예제: 스토리지 계정 만들기(기본 종류 변경)  

  이전:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  이후:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
