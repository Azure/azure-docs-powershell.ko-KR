---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 214b43148020b2884013a45f26b4a03cd4ea3736
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971280"
---
# <span data-ttu-id="7c254-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7c254-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7c254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c254-102">SYNOPSIS</span></span>
<span data-ttu-id="7c254-103">디바이스에 대한 저장소 계정 자격 증명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c254-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="7c254-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c254-104">SYNTAX</span></span>

### <span data-ttu-id="7c254-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7c254-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c254-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c254-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c254-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c254-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c254-108">설명</span><span class="sxs-lookup"><span data-stu-id="7c254-108">DESCRIPTION</span></span>
<span data-ttu-id="7c254-109">**Set-AzDataBoxEdgeStorageAccountCredential** cmdlet은 Data Box Edge 디바이스의 저장소 계정에 해당하는 저장소 계정 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7c254-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="7c254-110">예제</span><span class="sxs-lookup"><span data-stu-id="7c254-110">EXAMPLES</span></span>

### <span data-ttu-id="7c254-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c254-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="7c254-112">저장소 계정에 대한 액세스 키를 회전하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c254-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="7c254-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c254-113">PARAMETERS</span></span>

### <span data-ttu-id="7c254-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c254-114">-AsJob</span></span>
<span data-ttu-id="7c254-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c254-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c254-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c254-116">-DefaultProfile</span></span>
<span data-ttu-id="7c254-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c254-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c254-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7c254-118">-DeviceName</span></span>
<span data-ttu-id="7c254-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="7c254-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c254-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7c254-120">-EncryptionKey</span></span>
<span data-ttu-id="7c254-121">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="7c254-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c254-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c254-122">-InputObject</span></span>
<span data-ttu-id="7c254-123">입력 개체</span><span class="sxs-lookup"><span data-stu-id="7c254-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c254-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7c254-124">-Name</span></span>
<span data-ttu-id="7c254-125">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="7c254-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c254-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c254-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c254-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7c254-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c254-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c254-128">-ResourceId</span></span>
<span data-ttu-id="7c254-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c254-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c254-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="7c254-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="7c254-131">저장소 계정 액세스 키 제공</span><span class="sxs-lookup"><span data-stu-id="7c254-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c254-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7c254-132">-Confirm</span></span>
<span data-ttu-id="7c254-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c254-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c254-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c254-134">-WhatIf</span></span>
<span data-ttu-id="7c254-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c254-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c254-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c254-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c254-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c254-137">CommonParameters</span></span>
<span data-ttu-id="7c254-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c254-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c254-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c254-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c254-140">입력</span><span class="sxs-lookup"><span data-stu-id="7c254-140">INPUTS</span></span>

### <span data-ttu-id="7c254-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7c254-141">System.String</span></span>

### <span data-ttu-id="7c254-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7c254-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7c254-143">출력</span><span class="sxs-lookup"><span data-stu-id="7c254-143">OUTPUTS</span></span>

### <span data-ttu-id="7c254-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7c254-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7c254-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c254-145">NOTES</span></span>

## <span data-ttu-id="7c254-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c254-146">RELATED LINKS</span></span>
