---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 163D2F00-E041-43A9-B077-9034F54B4F3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf258a8f13a344b09f9d5c7119cd78ad202d2ca0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045683"
---
# <span data-ttu-id="24f2a-101">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="24f2a-101">Enable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="24f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="24f2a-103">클라우드 서비스에 대 한 원격 데스크톱 액세스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-103">Enables remote desktop access to a cloud service.</span></span>

## <span data-ttu-id="24f2a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24f2a-104">SYNTAX</span></span>

```
Enable-AzureServiceProjectRemoteDesktop -Username <String> -Password <SecureString> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="24f2a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="24f2a-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="24f2a-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="24f2a-108">**-AzureServiceProjectRemoteDesktop** Cmdlet을 사용 하면 클라우드 서비스에 대 한 원격 데스크톱 액세스를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-108">The **Enable-AzureServiceProjectRemoteDesktop** cmdlet enables Remote Desktop access to a cloud service.</span></span>
<span data-ttu-id="24f2a-109">원격 데스크톱 액세스를 사용 하도록 설정한 후에는 **게시-AzureServiceProject** cmdlet을 사용 하 여 서비스를 게시 해야 변경 내용이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after enabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="24f2a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="24f2a-110">EXAMPLES</span></span>

## <span data-ttu-id="24f2a-111">변수</span><span class="sxs-lookup"><span data-stu-id="24f2a-111">PARAMETERS</span></span>

### <span data-ttu-id="24f2a-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24f2a-112">-PassThru</span></span>
<span data-ttu-id="24f2a-113">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="24f2a-114">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f2a-115">-암호</span><span class="sxs-lookup"><span data-stu-id="24f2a-115">-Password</span></span>
<span data-ttu-id="24f2a-116">암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-116">Specifies the password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: pwd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f2a-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="24f2a-117">-Profile</span></span>
<span data-ttu-id="24f2a-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="24f2a-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="24f2a-120">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="24f2a-120">-Username</span></span>
<span data-ttu-id="24f2a-121">RDP (원격 데스크톱 프로토콜)를 통해 Azure에서 역할 인스턴스에 연결할 때 사용할 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-121">Specifies the user name to use when connecting to the role instance in Azure via the Remote Desktop Protocol (RDP).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: user

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f2a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f2a-122">CommonParameters</span></span>
<span data-ttu-id="24f2a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24f2a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f2a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24f2a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f2a-125">입력</span><span class="sxs-lookup"><span data-stu-id="24f2a-125">INPUTS</span></span>

## <span data-ttu-id="24f2a-126">출력</span><span class="sxs-lookup"><span data-stu-id="24f2a-126">OUTPUTS</span></span>

## <span data-ttu-id="24f2a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="24f2a-127">NOTES</span></span>

## <span data-ttu-id="24f2a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24f2a-128">RELATED LINKS</span></span>

[<span data-ttu-id="24f2a-129">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="24f2a-129">Disable-AzureServiceProjectRemoteDesktop</span></span>](./Disable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="24f2a-130">게시-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="24f2a-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


