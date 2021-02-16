---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200268"
---
# New-AzHDInsightClusterConfig

## SYNOPSIS
Azure HDInsight 클러스터 구성을 설명하는 비 지속형 클러스터 구성 개체를 만듭니다.

## 구문

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzHDInsightClusterConfig** cmdlet은 Azure HDInsight 클러스터 구성을 설명하는 비 지속형 개체를 만듭니다.

## 예제

### 예제 1: 클러스터 구성 개체 만들기
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

이 명령은 클러스터 구성 개체를 만듭니다.

## PARAMETERS

### -AadTenantId
Azure Data Lake Store에 액세스할 때 사용할 Azure AD 테넌트 ID를 지정합니다.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
Azure Data Lake에 액세스하기 위한 서비스 주체 애플리케이션 ID를 얻거나 설정합니다.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignedIdentity
할당된 ID를 얻거나 설정합니다.

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

### -CertificateFileContents
Azure Data Lake Store에 액세스할 때 사용할 인증서의 파일 콘텐츠를 지정합니다.

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateFilePath
서비스 주체로 인증하는 데 사용할 인증서의 파일 경로를 지정합니다.
클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.

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

### -CertificatePassword
서비스 주체로 인증하는 데 사용할 인증서의 암호를 지정합니다.
클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.

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

### -ClusterTier
HDInsight 클러스터 계층을 지정합니다.
이 매개 변수에 허용되는 값은
- 표준
- Premium 기본값은 Standard입니다.
프리미엄 계층은 Linux 클러스터에서만 사용할 수 있으며 몇 가지 새로운 기능을 사용할 수 있습니다.

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterType
만들 클러스터의 유형을 지정합니다.
이 매개 변수에 허용되는 값은
- Hadoop
- HBase
- Storm
- Spark
- INTERACTIVEHIVE
- Kafka
- RServer

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

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -EdgeNodeSize
에지 노드에 대한 가상 머신의 크기를 지정합니다. 허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요. 이 매개 변수는 RServer 클러스터에만 유효합니다.

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

### -EncryptionAlgorithm
암호화 알고리즘을 얻거나 설정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
호스트에서 암호화를 사용할지 여부를 나타내는 플래그를 얻거나 설정합니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionInTransit
전송 중 암호화를 사용할지 여부를 나타내는 플래그를 얻거나 설정합니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyName
암호화 키 이름을 얻거나 설정합니다.

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

### -EncryptionKeyVersion
암호화 키 버전을 얻거나 설정합니다.

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

### -EncryptionVaultUri
암호화 자격 증명 모음 URI를 얻거나 설정합니다.

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

### -HeadNodeSize
헤드 노드에 대한 가상 머신의 크기를 지정합니다.
허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.

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

### -HiveMetastore
Hive 메타데이터를 저장할 metastore를 지정합니다.
또는 Add-AzHDInsightMetastore cmdlet을 사용할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinSupportedTlsVersion
지원되는 최소 TLS 버전을 얻거나 설정합니다.

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

### -ObjectId
클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID(GUID)를 지정합니다.
클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OozieMetastore
Oozie 메타데이터를 저장할 metastore를 지정합니다.
또는 **Add-AzHDInsightMetastore** cmdlet을 사용할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
저장소 계정 액세스 키를 얻거나 설정합니다.

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

### -StorageAccountResourceId
저장소 계정 리소스 ID를 얻거나 설정합니다.

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

### -StorageAccountType
기본 저장소 계정의 유형을 얻거나 설정합니다.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkerNodeSize
Worker 노드에 대한 가상 머신의 크기를 지정합니다.
허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.

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

### -ZookeeperNodeSize
Zookeeper 노드에 대한 가상 머신의 크기를 지정합니다.
허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.
이 매개 변수는 HBase 또는 Storm 클러스터에만 유효합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig

## 참고 사항

## 관련 링크

[Add-AzHDInsightStorage](./Add-AzHDInsightStorage.md)


