---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046240"
---
# <span data-ttu-id="75b18-101">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="75b18-101">Move-AzureService</span></span>

## <span data-ttu-id="75b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75b18-102">SYNOPSIS</span></span>
<span data-ttu-id="75b18-103">클라우드 서비스를 Azure 리소스 관리자 스택으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-103">Migrates a cloud service to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="75b18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75b18-104">SYNTAX</span></span>

### <span data-ttu-id="75b18-105">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="75b18-105">AbortMigrationParameterSet</span></span>
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="75b18-106">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="75b18-106">CommitMigrationParameterSet</span></span>
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="75b18-107">PrepareNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="75b18-107">PrepareNewMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="75b18-108">PrepareExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="75b18-108">PrepareExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="75b18-109">ValidateNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="75b18-109">ValidateNewMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="75b18-110">ValidateExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="75b18-110">ValidateExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="75b18-111">설명은</span><span class="sxs-lookup"><span data-stu-id="75b18-111">DESCRIPTION</span></span>
<span data-ttu-id="75b18-112">**이동-azureservice** cmdlet은 클라우드 서비스와 해당 서비스 내의 배포를 Azure 리소스 관리자 스택의 리소스 그룹으로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-112">The **Move-AzureService** cmdlet migrates a cloud service and a deployment inside that service to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="75b18-113">예제의</span><span class="sxs-lookup"><span data-stu-id="75b18-113">EXAMPLES</span></span>

### <span data-ttu-id="75b18-114">예제 1: 서비스 마이그레이션 준비</span><span class="sxs-lookup"><span data-stu-id="75b18-114">Example 1: Prepare service migration</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="75b18-115">이 명령은 ContosoService 라는 서비스를 Azure Resource Manager 스택으로 마이그레이션하도록 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-115">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="75b18-116">마이그레이션에는 ContosoVM 이라는 배포가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-116">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="75b18-117">예제 2: 서비스 마이그레이션 시작</span><span class="sxs-lookup"><span data-stu-id="75b18-117">Example 2: Start service migration</span></span>
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="75b18-118">이 명령은 ContosoService 이라는 서비스를 Azure 리소스 관리자 스택으로 마이그레이션하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-118">This command starts migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="75b18-119">마이그레이션에는 ContosoVM 이라는 배포가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-119">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="75b18-120">예제 3: 서비스 마이그레이션 취소</span><span class="sxs-lookup"><span data-stu-id="75b18-120">Example 3: Cancel service migration</span></span>
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="75b18-121">이 명령은 ContosoService 이라는 서비스의 마이그레이션을 취소 하 여 Azure Resource Manager 스택에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-121">This command cancels migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="75b18-122">예제 4: 기존 가상 네트워크에 대 한 서비스 마이그레이션 준비</span><span class="sxs-lookup"><span data-stu-id="75b18-122">Example 4: Prepare service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="75b18-123">이 명령은 ContosoService 라는 서비스를 Azure Resource Manager 스택으로 마이그레이션하도록 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-123">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="75b18-124">마이그레이션에는 ContosoVM 이라는 배포가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-124">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="75b18-125">마이그레이션에서는 이전에 만든 가상 네트워크를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-125">The migration uses a virtual network that was previously created.</span></span>

### <span data-ttu-id="75b18-126">예제 5: 서비스 마이그레이션 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="75b18-126">Example 5: Validate service migration</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="75b18-127">이 명령은 ContosoService 이라는 서비스에 대 한 마이그레이션을 유효성 검사 하 여 Azure Resource Manager 스택에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-127">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="75b18-128">마이그레이션에는 ContosoVM 이라는 배포가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-128">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="75b18-129">예제 6: 기존 가상 네트워크에 대 한 서비스 마이그레이션 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="75b18-129">Example 6: Validate service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

<span data-ttu-id="75b18-130">이 명령은 ContosoService 이라는 서비스에 대 한 마이그레이션을 유효성 검사 하 여 Azure Resource Manager 스택에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-130">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="75b18-131">마이그레이션에는 ContosoVM 이라는 배포가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-131">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="75b18-132">마이그레이션에서는 이전에 만든 가상 네트워크를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-132">The migration uses a virtual network that was previously created.</span></span>

## <span data-ttu-id="75b18-133">변수</span><span class="sxs-lookup"><span data-stu-id="75b18-133">PARAMETERS</span></span>

### <span data-ttu-id="75b18-134">-Abort</span><span class="sxs-lookup"><span data-stu-id="75b18-134">-Abort</span></span>
<span data-ttu-id="75b18-135">이 cmdlet이 서비스 마이그레이션을 취소 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-135">Indicates that this cmdlet cancels the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-136">-커밋</span><span class="sxs-lookup"><span data-stu-id="75b18-136">-Commit</span></span>
<span data-ttu-id="75b18-137">이 cmdlet이 서비스 마이그레이션을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-137">Indicates that this cmdlet starts the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-138">-CreateNewVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75b18-138">-CreateNewVirtualNetwork</span></span>
<span data-ttu-id="75b18-139">이 cmdlet이 Azure Resource Manager 스택에 가상 네트워크를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-139">Indicates that this cmdlet creates a virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-140">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="75b18-140">-DeploymentName</span></span>
<span data-ttu-id="75b18-141">이 cmdlet이 마이그레이션하는 클라우드 서비스 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-141">Specifies the name of the cloud service deployment that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-142">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="75b18-142">-InformationAction</span></span>
<span data-ttu-id="75b18-143">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-143">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="75b18-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75b18-145">하기로</span><span class="sxs-lookup"><span data-stu-id="75b18-145">Continue</span></span>
- <span data-ttu-id="75b18-146">숨기기</span><span class="sxs-lookup"><span data-stu-id="75b18-146">Ignore</span></span>
- <span data-ttu-id="75b18-147">Inquire</span><span class="sxs-lookup"><span data-stu-id="75b18-147">Inquire</span></span>
- <span data-ttu-id="75b18-148">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="75b18-148">SilentlyContinue</span></span>
- <span data-ttu-id="75b18-149">중지가</span><span class="sxs-lookup"><span data-stu-id="75b18-149">Stop</span></span>
- <span data-ttu-id="75b18-150">대기</span><span class="sxs-lookup"><span data-stu-id="75b18-150">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-151">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="75b18-151">-InformationVariable</span></span>
<span data-ttu-id="75b18-152">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-152">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-153">-준비</span><span class="sxs-lookup"><span data-stu-id="75b18-153">-Prepare</span></span>
<span data-ttu-id="75b18-154">이 cmdlet이 클라우드 서비스 마이그레이션을 준비 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-154">Indicates that this cmdlet prepares the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-155">-프로필</span><span class="sxs-lookup"><span data-stu-id="75b18-155">-Profile</span></span>
<span data-ttu-id="75b18-156">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75b18-157">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="75b18-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="75b18-158">-ServiceName</span></span>
<span data-ttu-id="75b18-159">이 cmdlet이 마이그레이션하는 클라우드 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-159">Specifies the name  of the cloud service that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-160">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="75b18-160">-SubnetName</span></span>
<span data-ttu-id="75b18-161">가상 네트워크 내부의 서브넷 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-161">Specifies the name of the Subnet inside the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-162">-UseExistingVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75b18-162">-UseExistingVirtualNetwork</span></span>
<span data-ttu-id="75b18-163">이 cmdlet이 클라우드 서비스를 Azure Resource Manager 스택의 기존 가상 네트워크로 마이그레이션하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-163">Indicates that this cmdlet migrates the cloud service to an existing virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-164">-유효성 검사</span><span class="sxs-lookup"><span data-stu-id="75b18-164">-Validate</span></span>
<span data-ttu-id="75b18-165">이 cmdlet이 마이그레이션에 대 한 클라우드 서비스의 유효성을 검사 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-165">Specifies that this cmdlet validates the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-166">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="75b18-166">-VirtualNetworkName</span></span>
<span data-ttu-id="75b18-167">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-167">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-168">-VirtualNetworkResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b18-168">-VirtualNetworkResourceGroupName</span></span>
<span data-ttu-id="75b18-169">기존 가상 네트워크의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-169">Specifies the name of the resource group of an existing virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b18-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b18-170">CommonParameters</span></span>
<span data-ttu-id="75b18-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b18-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b18-172">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b18-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b18-173">입력</span><span class="sxs-lookup"><span data-stu-id="75b18-173">INPUTS</span></span>

## <span data-ttu-id="75b18-174">출력</span><span class="sxs-lookup"><span data-stu-id="75b18-174">OUTPUTS</span></span>

## <span data-ttu-id="75b18-175">상속자</span><span class="sxs-lookup"><span data-stu-id="75b18-175">NOTES</span></span>

## <span data-ttu-id="75b18-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75b18-176">RELATED LINKS</span></span>

[<span data-ttu-id="75b18-177">이동-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="75b18-177">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="75b18-178">이동-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="75b18-178">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="75b18-179">이동-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="75b18-179">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="75b18-180">이동-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75b18-180">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="75b18-181">이동-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75b18-181">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


