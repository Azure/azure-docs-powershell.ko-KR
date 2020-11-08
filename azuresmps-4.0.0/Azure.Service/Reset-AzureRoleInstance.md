---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045480"
---
# <span data-ttu-id="b1075-101">Reset-AzureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="b1075-101">Reset-AzureRoleInstance</span></span>

## <span data-ttu-id="b1075-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1075-102">SYNOPSIS</span></span>
<span data-ttu-id="b1075-103">특정 역할의 단일 역할 인스턴스 또는 모든 역할 인스턴스의 재부팅 또는 다시 부팅을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-103">Requests a reboot or reimage of a single role instance or all role instances of a specific role.</span></span>

## <span data-ttu-id="b1075-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1075-104">SYNTAX</span></span>

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1075-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1075-105">DESCRIPTION</span></span>
<span data-ttu-id="b1075-106">**AzureRoleInstance** cmdlet은 배포에서 실행 되는 역할 인스턴스의 다시 부팅을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-106">The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.</span></span>
<span data-ttu-id="b1075-107">이 작업은 동기적으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-107">This operation executes synchronously.</span></span>
<span data-ttu-id="b1075-108">역할 인스턴스를 다시 부팅 하면 Azure에서 해당 인스턴스를 오프 라인 상태로 전환 하 고 해당 인스턴스에 대 한 기본 운영 체제를 다시 시작 하 고 인스턴스를 다시 온라인 상태로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-108">When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.</span></span>
<span data-ttu-id="b1075-109">로컬 디스크에 기록 된 모든 데이터는 다시 부팅 하는 동안 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-109">Any data that is written to the local disk persists across reboots.</span></span>
<span data-ttu-id="b1075-110">메모리 내에 있는 모든 데이터는 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-110">Any data that is in-memory is lost.</span></span>

<span data-ttu-id="b1075-111">역할 인스턴스가 Reimaging 역할 유형에 따라 다른 동작이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-111">Reimaging a role instance results in different behavior depending on the type of role.</span></span>
<span data-ttu-id="b1075-112">웹 또는 작업자 역할의 경우 역할이 reimaged 경우 Azure가 오프 라인으로 전환 하 고 Azure 게스트 운영 체제의 새 설치를 가상 컴퓨터에 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-112">For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.</span></span>
<span data-ttu-id="b1075-113">그러면 역할이 다시 온라인 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-113">The role is then brought back online.</span></span>
<span data-ttu-id="b1075-114">VM 역할의 경우 역할을 reimaged 하는 경우 Azure가 오프 라인으로 전환 하 고, 제공 된 사용자 지정 이미지를 다시 적용 하 고, 역할을 온라인 상태로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-114">For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.</span></span>

<span data-ttu-id="b1075-115">Azure는 역할이 reimaged 때 로컬 저장소 리소스에 데이터를 유지 관리 하려고 시도 합니다. 그러나 일시적인 하드웨어 장애가 발생 하는 경우 로컬 저장소 리소스가 손실 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-115">Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.</span></span>
<span data-ttu-id="b1075-116">응용 프로그램에서 Azure 드라이브와 같은 영속적 데이터 원본에 기록 하는 데이터를 유지 해야 하는 경우 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-116">If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.</span></span>
<span data-ttu-id="b1075-117">로컬 저장소 리소스에 정의 된 것과는 다른 로컬 디렉터리에 기록 된 데이터는 역할이 reimaged 경우 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-117">Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.</span></span>

## <span data-ttu-id="b1075-118">예제의</span><span class="sxs-lookup"><span data-stu-id="b1075-118">EXAMPLES</span></span>

### <span data-ttu-id="b1075-119">예제 1: 역할 인스턴스 다시 부팅</span><span class="sxs-lookup"><span data-stu-id="b1075-119">Example 1: Reboot a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

<span data-ttu-id="b1075-120">이 명령은 MySvc01 서비스의 스테이징 배포에서 MyWebRole_IN_0 이라는 역할 인스턴스를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-120">This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.</span></span>

### <span data-ttu-id="b1075-121">예제 2: 역할 인스턴스를 이미지로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-121">Example 2: Reimage a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

<span data-ttu-id="b1075-122">이 명령은 MySvc01 클라우드 서비스의 스테이징 배포에서 역할 인스턴스를 다시 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-122">This command reimages the role instances in the staging deployment of the MySvc01 cloud service.</span></span>

### <span data-ttu-id="b1075-123">예제 3: 모든 역할 인스턴스 이미지로</span><span class="sxs-lookup"><span data-stu-id="b1075-123">Example 3: Reimage all role instances</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

<span data-ttu-id="b1075-124">이 명령은 MySvc01 서비스의 프로덕션 배포에 있는 모든 역할 인스턴스를 다시 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-124">This command reimages all role instances in the production deployment of the MySvc01 service.</span></span>

## <span data-ttu-id="b1075-125">변수</span><span class="sxs-lookup"><span data-stu-id="b1075-125">PARAMETERS</span></span>

### <span data-ttu-id="b1075-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b1075-126">-InformationAction</span></span>
<span data-ttu-id="b1075-127">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b1075-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1075-129">하기로</span><span class="sxs-lookup"><span data-stu-id="b1075-129">Continue</span></span>
- <span data-ttu-id="b1075-130">숨기기</span><span class="sxs-lookup"><span data-stu-id="b1075-130">Ignore</span></span>
- <span data-ttu-id="b1075-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="b1075-131">Inquire</span></span>
- <span data-ttu-id="b1075-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b1075-132">SilentlyContinue</span></span>
- <span data-ttu-id="b1075-133">중지가</span><span class="sxs-lookup"><span data-stu-id="b1075-133">Stop</span></span>
- <span data-ttu-id="b1075-134">대기</span><span class="sxs-lookup"><span data-stu-id="b1075-134">Suspend</span></span>

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

### <span data-ttu-id="b1075-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b1075-135">-InformationVariable</span></span>
<span data-ttu-id="b1075-136">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b1075-137">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b1075-137">-InstanceName</span></span>
<span data-ttu-id="b1075-138">다시 부팅 하거나 재부팅할 역할 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-138">Specifies the name of the role instance to reimage or reboot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1075-139">-프로필</span><span class="sxs-lookup"><span data-stu-id="b1075-139">-Profile</span></span>
<span data-ttu-id="b1075-140">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1075-141">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1075-142">-다시 부팅</span><span class="sxs-lookup"><span data-stu-id="b1075-142">-Reboot</span></span>
<span data-ttu-id="b1075-143">이 cmdlet이 지정 된 역할 인스턴스를 재부팅 하도록 지정 하거나 지정 하지 않은 경우 모든 역할 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-143">Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="b1075-144">*Reboot* 또는 *이미지로* 매개 변수 중 하나만 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-144">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

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

### <span data-ttu-id="b1075-145">-이미지로</span><span class="sxs-lookup"><span data-stu-id="b1075-145">-Reimage</span></span>
<span data-ttu-id="b1075-146">이 cmdlet이 지정 된 역할 인스턴스를 다시 이미지 하도록 지정 하거나 지정 하지 않은 경우 모든 역할 인스턴스를 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-146">Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="b1075-147">*Reboot* 또는 *이미지로* 매개 변수 중 하나만 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-147">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

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

### <span data-ttu-id="b1075-148">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b1075-148">-ServiceName</span></span>
<span data-ttu-id="b1075-149">서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-149">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1075-150">-슬롯</span><span class="sxs-lookup"><span data-stu-id="b1075-150">-Slot</span></span>
<span data-ttu-id="b1075-151">역할 인스턴스가 실행 되는 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-151">Specifies the deployment environment where the role instances run.</span></span>
<span data-ttu-id="b1075-152">유효한 값은 프로덕션 및 준비입니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-152">Valid values are: Production and Staging.</span></span>
<span data-ttu-id="b1075-153">*Deploymentname* 또는 *Slot* 매개 변수 중 하나만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-153">You can include either the *DeploymentName* or *Slot* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1075-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1075-154">CommonParameters</span></span>
<span data-ttu-id="b1075-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1075-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1075-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1075-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1075-157">입력</span><span class="sxs-lookup"><span data-stu-id="b1075-157">INPUTS</span></span>

## <span data-ttu-id="b1075-158">출력</span><span class="sxs-lookup"><span data-stu-id="b1075-158">OUTPUTS</span></span>

## <span data-ttu-id="b1075-159">상속자</span><span class="sxs-lookup"><span data-stu-id="b1075-159">NOTES</span></span>

## <span data-ttu-id="b1075-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1075-160">RELATED LINKS</span></span>

[<span data-ttu-id="b1075-161">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="b1075-161">Set-AzureRole</span></span>](./Set-AzureRole.md)


