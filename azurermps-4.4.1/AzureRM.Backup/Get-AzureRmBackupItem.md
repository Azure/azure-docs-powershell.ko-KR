---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 543aa3e28d7f3dee20065a0d20f2429b3fd6d4f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527716"
---
# <span data-ttu-id="cdeef-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="cdeef-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="cdeef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdeef-102">SYNOPSIS</span></span>
<span data-ttu-id="cdeef-103">백업의 컨테이너 아래에 있는 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdeef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cdeef-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdeef-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cdeef-105">DESCRIPTION</span></span>
<span data-ttu-id="cdeef-106">**AzureRmBackupItem** Cmdlet은 Azure Backup의 컨테이너에 있는 항목과 항목의 보호 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="cdeef-107">Enable-AzureRmBackupProtection cmdlet을 사용 하 여 항목을 보호할 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>

<span data-ttu-id="cdeef-108">백업 자격 증명 모음에 등록 된 컨테이너에는 보호할 수 있는 항목이 하나 이상 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="cdeef-109">Azure 가상 컴퓨터의 경우 가상 컴퓨터 컨테이너에 항목이 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="cdeef-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cdeef-110">EXAMPLES</span></span>

### <span data-ttu-id="cdeef-111">예제 1: 컨테이너에서 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="cdeef-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="cdeef-112">첫 번째 명령은 Get-AzureRmBackupVault cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="cdeef-113">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="cdeef-114">두 번째 명령은 **AzureRmBackupContainer** cmdlet을 사용 하 여 $Vault의 자격 증명 모음에서 지정 된 이름을 가진 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="cdeef-115">명령이 $Container 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-115">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="cdeef-116">마지막 명령은 $Container의 컨테이너에 있는 백업 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="cdeef-117">예제 2: 항목의 모든 속성 보기</span><span class="sxs-lookup"><span data-stu-id="cdeef-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="cdeef-118">이 명령은 $Container에서 컨테이너의 백업 항목을 가져온 다음 Select-Object cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="cdeef-119">해당 cmdlet은 백업 항목의 모든 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="cdeef-120">자세한 내용은을 입력 `Get-Help Select-Object` 하세요.</span><span class="sxs-lookup"><span data-stu-id="cdeef-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="cdeef-121">변수</span><span class="sxs-lookup"><span data-stu-id="cdeef-121">PARAMETERS</span></span>

### <span data-ttu-id="cdeef-122">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="cdeef-122">-Container</span></span>
<span data-ttu-id="cdeef-123">이 cmdlet에서 백업 항목을 가져오는 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="cdeef-124">**AzureRmBackupContainer** 을 얻으려면 Get-AzureRmBackupContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdeef-125">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="cdeef-125">-ProtectionStatus</span></span>
<span data-ttu-id="cdeef-126">컨테이너에 있는 항목의 전체 보호 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-126">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="cdeef-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cdeef-128">됨</span><span class="sxs-lookup"><span data-stu-id="cdeef-128">Protected</span></span> 
- <span data-ttu-id="cdeef-129">방지</span><span class="sxs-lookup"><span data-stu-id="cdeef-129">Protecting</span></span>  
- <span data-ttu-id="cdeef-130">NotProtected</span><span class="sxs-lookup"><span data-stu-id="cdeef-130">NotProtected</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdeef-131">-상태</span><span class="sxs-lookup"><span data-stu-id="cdeef-131">-Status</span></span>
<span data-ttu-id="cdeef-132">항목의 백업 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-132">Specifies the backup status for an item.</span></span>
<span data-ttu-id="cdeef-133">이 매개 변수에 허용 되는 값은 IRPending, Protected, ProtectionError 및 ProtectionStopped입니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-133">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="cdeef-134">*ProtectionStatus* 매개 변수에 보호 된 값이 있는 경우 *Status* 매개 변수 값을 사용 하 여 항목을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-134">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdeef-135">-Type</span><span class="sxs-lookup"><span data-stu-id="cdeef-135">-Type</span></span>
<span data-ttu-id="cdeef-136">이 cmdlet이 가져오는 항목의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-136">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="cdeef-137">현재만 지원 되는 값은 Add-azurevm입니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-137">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdeef-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdeef-138">-DefaultProfile</span></span>
<span data-ttu-id="cdeef-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdeef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdeef-140">CommonParameters</span></span>
<span data-ttu-id="cdeef-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdeef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdeef-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdeef-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdeef-143">입력</span><span class="sxs-lookup"><span data-stu-id="cdeef-143">INPUTS</span></span>

### <span data-ttu-id="cdeef-144">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="cdeef-144">AzureRmBackupContainer</span></span>

## <span data-ttu-id="cdeef-145">출력</span><span class="sxs-lookup"><span data-stu-id="cdeef-145">OUTPUTS</span></span>

### <span data-ttu-id="cdeef-146">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="cdeef-146">AzureRmBackupItem</span></span>

## <span data-ttu-id="cdeef-147">상속자</span><span class="sxs-lookup"><span data-stu-id="cdeef-147">NOTES</span></span>

## <span data-ttu-id="cdeef-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cdeef-148">RELATED LINKS</span></span>

[<span data-ttu-id="cdeef-149">백업-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="cdeef-149">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="cdeef-150">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="cdeef-150">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="cdeef-151">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="cdeef-151">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="cdeef-152">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="cdeef-152">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="cdeef-153">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="cdeef-153">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="cdeef-154">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="cdeef-154">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


