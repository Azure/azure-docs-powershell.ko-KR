---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E735FCE5-D82F-42D0-8D74-6A568E55AC17
online version: ''
schema: 2.0.0
ms.openlocfilehash: 433a50a93f8fa8e68021d09d5c1ae464703e227c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045696"
---
# <span data-ttu-id="a6fe2-101">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="a6fe2-101">Disable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="a6fe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="a6fe2-103">클라우드 서비스에 대 한 원격 데스크톱 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6fe2-103">Disables Remote Desktop access to a cloud service.</span></span>

## <span data-ttu-id="a6fe2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6fe2-104">SYNTAX</span></span>

```
Disable-AzureServiceProjectRemoteDesktop [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a6fe2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a6fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="a6fe2-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6fe2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a6fe2-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6fe2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a6fe2-108">**-AzureServiceProjectRemoteDesktop** 은 호스팅된 서비스에 대 한 원격 데스크톱 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6fe2-108">The **Disable-AzureServiceProjectRemoteDesktop** disables remote desktop access to a hosted service.</span></span>
<span data-ttu-id="a6fe2-109">변경 내용을 적용 하려면 원격 데스크톱 액세스를 사용 하지 않도록 설정한 후 **게시-AzureServiceProject** cmdlet을 사용 하 여 서비스를 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6fe2-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after disabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="a6fe2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a6fe2-110">EXAMPLES</span></span>

## <span data-ttu-id="a6fe2-111">변수</span><span class="sxs-lookup"><span data-stu-id="a6fe2-111">PARAMETERS</span></span>

### <span data-ttu-id="a6fe2-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6fe2-112">-PassThru</span></span>
<span data-ttu-id="a6fe2-113">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6fe2-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a6fe2-114">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6fe2-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a6fe2-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="a6fe2-115">-Profile</span></span>
<span data-ttu-id="a6fe2-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6fe2-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a6fe2-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a6fe2-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6fe2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6fe2-118">CommonParameters</span></span>
<span data-ttu-id="a6fe2-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6fe2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6fe2-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6fe2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6fe2-121">입력</span><span class="sxs-lookup"><span data-stu-id="a6fe2-121">INPUTS</span></span>

## <span data-ttu-id="a6fe2-122">출력</span><span class="sxs-lookup"><span data-stu-id="a6fe2-122">OUTPUTS</span></span>

## <span data-ttu-id="a6fe2-123">상속자</span><span class="sxs-lookup"><span data-stu-id="a6fe2-123">NOTES</span></span>

## <span data-ttu-id="a6fe2-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6fe2-124">RELATED LINKS</span></span>

[<span data-ttu-id="a6fe2-125">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="a6fe2-125">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)


